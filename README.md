# django-project2
2th django project using MySQL and bootstrap


index:
![Captura de tela 2024-11-24 001043](https://github.com/user-attachments/assets/e66ba17b-2d87-4e3b-8dfe-faa29685d229)
![Captura de tela 2024-11-24 001153](https://github.com/user-attachments/assets/6a063304-71f1-4bc7-9684-fa52cafca46e)

/produto:
![Captura de tela 2024-11-24 001608](https://github.com/user-attachments/assets/a8b2b9fd-74a4-4724-a2fd-1c53d560faf5)

/contato:
![Captura de tela 2024-11-24 001257](https://github.com/user-attachments/assets/ee954695-95df-4bc5-be32-f9862af7378d)


### 1. installing django and libraries:
     pip install django whitenoise gunicorn django-bootstrap4 PyMySQL django-stdimage
     pip freeze > requirements.txt

   
### 2. create project
     django-admin stratproject projectname .

     
### 3. create application
     django-admin startapp core
INSTALLED_APPS = [
           
           ...
          'core',
]

     
### 4. configure settings.py to start
 INSTALLED_APPS = [
    
    'core',
    'bootstrap4',
    'stdimage',
]
MIDDLEWARE =
[

    (#) 'whitenoise.middleware.WhiteNoiseMiddleware',
]
TEMPLATES = [

        'DIRS': ['templates'],
]
DATABASES = {

    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'django2',
        'USER': 'name',
        'PASSWORD': 'password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}

LANGUAGE_CODE = 'pt-br'

TIME_ZONE = 'America/Sao_Paulo'

STATIC_ROOT = os.path.join(BASE_DIR, 'static')


### 5. urls (project)
  
  path(' ', include('core.urls')),


### 6. urls (application)
  from django2.urls import path, urlpatterns
  
  from .views import index, contato, produto

urlpatterns = [

    path('', index, name='index'),
    path('contato/', contato, name='contato'),
    path('produto/', produto, name='produto'),
]


### 7. install MYSql
    pip install MySQL
    pip freeze > requirements.py


### 8. create superuser  
    python manage.py createsuperuser


### 9. runserver 
    python manage.py runserver


### 10.migrations
    python manage.py makemigrations
    python manage.py migrate
