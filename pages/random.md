---
title: Random
---

## #clojure #logseq tips
### We can customize the #journal page by adding macros in https://github.com/bayesianbrad/notes/blob/master/logseq/config.edn
### In particular, copy the templates:
####
```clojure 
;; The app will show those queries in today's journal page,
 ;; the "NOW" query asks the tasks which need to be finished "now",
 ;; the "NEXT" query asks the future tasks.
 :default-queries
 {:journals
  [{:title "🔨 NOW"
    :query [:find (pull ?h [*])
            :in $ ?start ?today
            :where
            [?h :block/marker ?marker]
            [?h :block/page ?p]
            [?p :page/journal? true]
            [?p :page/journal-day ?d]
            [(>= ?d ?start)]
            [(<= ?d ?today)]
            [(contains? #{"NOW" "DOING"} ?marker)]]
    :inputs [:14d :today]
    :result-transform (fn [result]
                        (sort-by (fn [h]
                                   (get h :block/priority "Z")) result))
    :collapsed? false}
   {:title "📅 NEXT"
    :query [:find (pull ?h [*])
            :in $ ?start ?next
            :where
            [?h :block/marker ?marker]
            [?h :block/ref-pages ?p]
            [?p :page/journal? true]
            [?p :page/journal-day ?d]
            [(> ?d ?start)]
            [(< ?d ?next)]
            [(contains? #{"NOW" "LATER" "TODO"} ?marker)]]
    :inputs [:today :7d-after]
    :collapsed? false}]}
```
####
#### We can run #javascript and add RSS directly in logseq pags, see here for details: https://github.com/71/logseq-snippets
####
