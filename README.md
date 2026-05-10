# Django Basic-Setup for beginner

At first, you have to install Python in your system, then let's create a Django application
Open your folder where you want to create the project and run this command
```
django-admin startproject yourProjectName
```

Create a virtual environment so that your project can run smoothly on it. You can get the latest version of pip, before that you should install virtualenv if it's not installed in your system. If it's already installed, just ignore this command

```
pip install virtualenv
```

And now it's time to set up a virtual environment on your Django app, open the Django app terminal, and run this command
```
python -m venv env
```
Now activate it
```
source env/Scripts/activate
```
If you want to deactivate the Virtual Environment
```
deactivate
```

After Activate env, install Django so that you can get the latest version of it
```
pip install django
```

And now check what packages are installed in your environment
```
pip freeze
```

Now you should run the Django project on the server, so that you can ensure that the project has been successfully run
```
python manage.py runserver
```

# Print Hello World on Django app home page

Create a views.py file in the Django app
In url.py, import this code
```
from projectName import views
```

in urlpatter list, include this URL path
```
path('', views.home)
```

In the views file, create a function named home
Import this package
```
from django.http import HttpResponse
```



```
def home (request):
    return HttpResponse("Hello World")
```

To render a page in Django, first create a template folder in the root, then write the template in settings.py. The code is below. Look at the template list in settings.py; here, you can see this code. Just insert the template

```
TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': ['templates'],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]
```

Create index.html in the template folder. After creating the HTML file, go to views.py and import this

```
from django.shortcuts import render
```

```
def home (request):
   return render(request, 'index.html')
```
