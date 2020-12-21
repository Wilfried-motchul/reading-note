# Django REST Framework

## Library Website and API
Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework; it always must be added to a project after Django itself has been installed and configured.

In this chapter we will review the similarities and differences between traditional Django and Django REST Framework. The most important takeaway is that Django creates websites containing webpages, while Django REST Framework creates web APIs which are a collection of URL endpoints containing available HTTP verbs that return JSON.

To illustrate these concepts, we will build out a basic Library website with traditional Django and then extend it into a web API with Django REST Framework.

Make sure you already have Python 3 and Pipenv installed on your computer. Complete instructions can be found here if you need help.

## Traditional Django

First we need a dedicated directory on our computer to store the code. This can live anywhere but for convenience, if you are on a Mac, we can place it in the Desktop folder. The location really does not matter; it just needs to be easily accessible.
```
$ cd ~/Desktop
$ mkdir code && cd code
```

Now we are within the `code` folder which will be the location for all the code in this book. The next step is to create a dedicated directory for our library site, install Django via Pipenv, and then enter the virtual environment using the `shell` command. You should always use a dedicated virtual environment for every new Python project.
```
$ mkdir library && cd library
$ pipenv install django~=3.1.0
$ pipenv shell
(library) $
```

Pipenv creates a `Pipfile` and a `Pipfile.lock` within our current directory. The `(library)`in parentheses before the command line shows that our virtual environment is active.

A traditional Django website consists of a single project and one (or more) apps representing discrete functionality. Let’s create a new project with the `startproject` command. Don’t forget to include the period . at the end which installs the code in our current directory. If you do not include the period, Django will create an additional directory by default.
```
(library) $ django-admin startproject config .
```

Django automatically generates a new project for us which we can see with the `tree` command. (Note: If tree doesn’t work for you on a Mac, install it with Homebrew: `brew install tree`.)
```
(library) $ tree
.
├── Pipfile
├── Pipfile.lock
├── config
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
└── manage.py
```

The files have the following roles:

* `__init__`.py is a Python way to treat a directory as a package; it is empty
* `asgi.py`stands for Asynchronous Server Gateway Interface and is a new option in Django 3.0+
* `settings.py` contains all the configuration for our project
* `urls.py` controls the top-level URL routes
* `wsgi.py` stands for Web Server Gateway Interface and helps Django serve the eventual web pages
* `manage.py` executes various Django commands such as running the local web server or creating a new app.

Run `migrate` to sync the database with Django’s default settings and start up the local Django web server.
```
(library) $ python manage.py migrate
(library) $ python manage.py runserver
```
Open a web browser to `http://127.0.0.1:8000/` to confirm our project is successfully installed.