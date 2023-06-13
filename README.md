# django-cheatsheet

An introduction to Django cheatsheet from CF Code41py


Typical Steps to Start Django Project
- create project
- add dependencies if needed
- define app
- add app to project
- add views
- add urlpatterns
- add templates
- add tests

---

- create/clone new repo
- change dir to repo

- create new virtual environment
  - `$ python3.11 -m venv .venv`

- activate virtual environment
  - `$ source .venv/bin/activate`

- ~create project folder~
  - ~$ mkdir django-things~

- ~change dir to project folder~
  - ~$ cd django-things~

- install django
  - `$ pip install django`

- create/start project
  - `$ django-admin startproject django_things_project .`

> - tree
    - asgi.py
    - __init__.py
    - settings.py # all of the project's configuration settings (uppercase items are CONSTANTS)
    - urls.py # routes for endpoints
    - wsgi.py

- run server (from inside the project folder)
  - `$ python manage.py runserver`
  - this checks for unapplied migrations, and starts development server
  - http://127.0.0.1:8000
    - "The install worked successfully. Congratulations!" proof-of-life

- apply all migrations
  - `$ python manage.py migrate`
  - `CTRL-C` to stop server before running this cmd

- `db.sqlite3` = default database
  - open in pycharm, then `refresh`

- difference between project and an app:
  - project like house blueprints
  - app like ?
  - separation of concerns?

- in the project start a new app called `things`
  - `$ python manage.py startapp things`

- register/connect the app to the project:
  - done in the project's settings.py file, in INSTALLED_APPS

views.py = callback functions ?

---

set-up Tailwind CSS (https://flowbite.com/docs/getting-started/django/):

- install django-compressor
  - `$ python -m pip install django-compressor`

- install Tailwind CSS as a dev dependency using NPM
  - `$ npm install -D tailwindscss`

- create a new tailwind.config.js file
  - `$ npx tailwindcss init`

- watch for changes and compile the Tailwind CSS code
  - `$ npx tailwindcss -i ./static/src/input.css -o ./static/src/output.css --watch`

- install Flowbite as a dependency using NPM
  - `$ npm install flowbite`

---

- run unit tests:
  - `$ python manage.py test`
