---
title: introtoflask
---

## #flask , unlike #django and other full-stack frameworks, does not impose a specific structure on the user. So you have to initiate it from scratch rather than call a command to build the directory structure. 

### A good structure to follow is:
#### - app.py
- static/
- templates/
#### Where `static/` houses the style sheets, #javascript files and images, while templates is for #html files.
#### [[Model-View-Controller]] is a design pattern that `app.py` will utilize in the back-end to handle requests and post responses to end users.
#### By breaking the app into these separate components, your business logic goes in `app.py` and front-end and back-end are separated.
### When we are `route`-ing webpages and `'GET'`ting and `'POST`ing requests we need to pass whatever logic is going to occur in the 
```python 
@app.route('/<some_page_name>', methods=['GET','POST'])
```
### `'GET'` is the default method. So if no methods are defined, #flask will assume that the only available method is `'GET'` i.e. if we specified:
```python 
@app.route('/<some_page_name>')
```
###
###
