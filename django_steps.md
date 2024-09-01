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

## steps to create an app
```
python manage.py startapp appname
```

## difference bw project and app in django

- project is the ENTIRE DJANGO APPLICATION
- app is a module inside the project that deals with one specific case

- for eg -- payment system (app) in eCommerce app (project)

- an app is basically a web application that is created to perform a specific task
- a project, on the other hand, is a collection of these apps

- therefore, a single project can consist of 'n' number of apps and a single app can be in multiple projects

### Explain How A Request Is Processed In Django?

- Here, a user requests for a resource to the Django, Django works as a controller and checks to the available resource in URL.
- When Django server is started, the `manage.py` file searches for `settings.py` file, which contains information of all the applications installed in the project, middleware used, database connections and path to the main URLs config.

![Django Request Process](./image.png)

- Django first determines which root URLconf or URL configuration module is to be used.
- Then, that particular Python module `urls` is loaded and then Django looks for the variable `urlpatterns`.
- Then check each URL pattern in `urls.py` file, and it stops at the first match of the requested URL.
- Once that is done, the Django then imports and calls the given view.
- In case none of the URLs match the requested URL, Django invokes an error-handling view.
- If URL maps, a view is called that interacts with the model and template, it renders a template.
- Django responds back to the user and sends a template as a response.
