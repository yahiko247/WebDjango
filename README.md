Steps in create a new project with Django + React vite.


1. Type this command 
py -m venv my_venv 
python -m venv my_venv

2. my_venv\Scripts\Activate

3. pip install django

4. if you have the old version just type python.exe -m pip install --upgrade pip

notice this messagme will appear if you have the old version of python.exe

[notice] A new release of pip is available: 24.0 -> 24.2

but you have the latest version skip this one

5. django-admin startproject backend

6. cd backend

7. django-admin startapp user_api

8. code .

9. go back to the terminal/cmd  type 
pip install djangorestframework

10. pip install django-cors-header


[i]creating api and configuration
1. Create a model inside user_api folder
2. creating endpoints in urls.py inside user_api folder
3. create a serializers.py inside user_api folder

4. create views
5. create validations.py inside user_api folder



[things to remind]
copy and paste this to your settings. This is some very important that other tutorials or documentations skips this steps.

1:
ALLOWED_HOSTS = ['*']

CORS_ORIGIN_ALLOW_ALL = True

CORS_ALLOW_CREDENTIALS = True

CORS_ALLOW_HEADERS = [
    'content-type',
    'authorization',
    'X-CSRFToken',
]

2:
AUTH_USER_MODEL = 'user_api.AppUser'


REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': (
        'rest_framework.permissions.IsAuthenticated',
    ),
    'DEFAULT_AUTHENTICATION_CLASSES': (
        'rest_framework.authentication.SessionAuthentication',
    ),
}




3: STATIC_ROOT = '/static/'






////
this ispart is creating the frontend for the project

1. go back to terminal and cd ..
2. type this command for creating new project in react vite
npm create vite@latest

give the name of the folder "frontend"

select react
select javascripts
3. cd frontend
4. npm install
5 install this two important dependencies 
npm install axios
npm install react-bootstrap bootstrap 


6. npm run dev
7. go back to terminal/ cmd type cd ..
8. code .





