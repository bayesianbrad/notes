---
title: Creating a database in Django
---

## By default #django uses [[SQLite]] - this is fine for messing around, but really you should use [[PostgreSQL]] or something similar.
### To change to a different database, you need to install the appropriate database bindings (see here: https://docs.djangoproject.com/en/3.1/topics/install/#database-installation)
### Then change the following kets in the `DATABASES 'default'` item to match your database connection settings, this is in `<project_name>/settings.py` file:
####
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3', # or could be: django.db.backends.postgresql for example. 
        'NAME': BASE_DIR / 'db.sqlite3', 
    }
}
```
#### For more details see: https://docs.djangoproject.com/en/3.1/ref/settings/#std:setting-DATABASES
#### Assuming database settings are complete run the following command to initiate some of the default applications in #django  that are stated in the `INSTALLED APPS` block of `settings.py`:
```shell
python manage.py migrate
```
### __Creating models__
#### A model is the single, definitive source of truth about your data. It contains the essential fields and behaviors of the data you’re storing. Django follows the [DRY](https://docs.djangoproject.com/en/3.1/misc/design-philosophies/#dry) Principle. The goal is to define your data model in one place and automatically derive things from it.
#### Every time you update your models, in `<application_name>/models.py` you need to run 
```shell
python manage.py makemigrations login
```
#### On running this command code is added to the `<application_name>/migration` which creates the database entries (kind of).
#### Migrations are how #django tracks changes to the model.
### In summary, there are three steps to making model changes:
- Change your models (in `models.py`).
- Run `python manage.py makemigrations` to create migrations for those changes
- Run `python manage.py` migrate to apply those changes to the database.
## For more information on model relations, see [Accessing related objects](https://docs.djangoproject.com/en/3.1/ref/models/relations/). For more on how to use double underscores to perform field lookups via the API, see Field lookups](https://docs.djangoproject.com/en/3.1/topics/db/queries/#field-lookups-intro). For full details on the database API, see our [Database API reference](https://docs.djangoproject.com/en/3.1/topics/db/queries/).
##
