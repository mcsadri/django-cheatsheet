# django-cheatsheet

An introduction to Django cheatsheet from CF Code41py

- create/clone new repo
- change dir to repo

- create new virtual environment
> $ python3.11 -m venv .venv

- activate virtual environment
> $ source .venv/bin/activate

- create project folder
> $ mkdir django-things

- change dir to project folder
> $ cd django-things

- install django
> $ pip install django

- start project
> $ django-admin startproject django_things_project .

> - tree
    - asgi.py
    - __init__.py
    - settings.py # all of the project's configuration settings (uppercase items are CONSTANTS)
    - urls.py # routes for endpoints
    - wsgi.py

- run server (from inside the project folder)
> $ python manage.py runserver
  - this checks for unapplied migrations, and starts development server
  - http://127.0.0.1:8000
    - "The install worked successfully. Congratulations!" proof-of-life

- apply all migrations
> $ python manage.py migrate
  - `CTRL-C` to stop server before running this cmd

- `db.sqlite3` = default database
  - open in pycharm, then `refresh`

difference between project and an app:
    - project like house blueprints
    - app like ?
    - separation of concerns?

- in the project start a new app called `things`
> $ python manage.py startapp things

- register/connect the app to the project:
  - done in the project's settings.py file, in INSTALLED_APPS




