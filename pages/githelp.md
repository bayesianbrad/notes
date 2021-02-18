---
title: githelp
---

## To remove large files, when accidentally committed and been partial pushed and `git reset --hard` does not work, run the following command 
```shell 
git filter-branch --tree-filter 'rm -rf path/to/your/file' HEAD
git push
```
##
