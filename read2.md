# Cape Craft Projects

![Cape Craft Projects Logo](https://durbanvilledistillery.com/images/CCLogo.png)

___

## Part 2 Development Flow

### Preparation

#### Make a directory for your project

md my project

#### Environments

Enables truly deterministic builds, while easily specifying only what you want.
Generates and checks file hashes for locked dependencies.

1. Automatically install required Pythons, if pyenv is available.
2. Automatically finds your project home, recursively, by looking for a Pipfile.
3. Automatically generates a Pipfile, if one doesn't exist.
4. Automatically creates a virtualenv in a standard location.
5. Automatically adds/removes packages to a Pipfile when they are un/installed.
6. Automatically loads .env files, if they exist

##### Setting up a Python environment is a good idea

If you are using a windows environment, you can use pipenv to create a virtual environment.
md my project
python -m pip install pipenv 3.8.0
python -m venv ./.venv
__
Select iterpreter (venv)
__
python -m pip install django
python -m pip freeze > requirements.txt
python -m pip freeze
python -m pip install -r requirements.txt
__

##### Setup Django Project

__

django-admin startproject xxxxx .
django-admin --version
pipenv install
pipenv shell
pipenv --venv

##### Run Django

python manage.py runserver
isort .
flake8 .
py manage.py test

### Sessions

1. Session is teporary and interactive information
2. Single user per session -save and retrieve arbitrary data on per visit basis
3. Store the data server side.
4. User receives a session ID
5. Session ID is used to retrieve the associated data.

py manaage.py shell
from django.contrib.sessions.models import Session

#### Enabling Sessions

INSTALLED_APPS = [
    'django.contrib.sessions',
]

MIDDLEWARE = [
    'django.contrib.sessions.middleware.SessionMiddleware',
]

#### Session Development - Part 1 - Add to Session

Setup
Create session
Context processor(site wide access)
Add to session functionality

## BUILDIING

1. Session py manage.py startapp basket
Trim unwanted files
2. Add to settings.py
basket>basket.py
![Part2](https://github.com/Cape-Craft-Projects/Django/tree/second_base220517)

requirements.txt
asgiref==3.3.1
autopep8==1.5.4
coverage==5.3.1
Django==3.1.4
flake8-django==1.1.1
isort==5.7.0
mccabe==0.6.1
Pillow==8.0.1
pycodestyle==2.6.0
pyflakes==2.2.0
pytz==2020.4
sqlparse==0.4.2
testfixtures==6.17.1
toml==0.10.2
