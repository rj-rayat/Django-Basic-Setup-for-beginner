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
