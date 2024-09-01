## steps to initiate a virtual environment
```
uv venv
source .venv/bin/activate
```
## steps to install Django
```
uv pip install Django
```
## steps to start a project
```
django-admin startproject projectname
cd projectname
```
## steps to run server
```
python manage.py runserver
```
## difference bw project and app in django

- project is the ENTIRE DJANGO APPLICATION
- app is a module inside the project that deals with one specific case

- for eg -- payment system (app) in eCommerce app (project)

- an app is basically a web application that is created to perform a specific task
- a project, on the other hand, is a collection of these apps

- therefore, a single project can consist of 'n' number of apps and a single app can be in multiple projects