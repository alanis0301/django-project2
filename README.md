# django-project2
2th project

1. instalação do django e das bibliotecas:
   pip install django whitenoise gunicorn django-bootstrap4 PyMySQL django-stdimage
   pip freeze > requirements.txt
2.criação do projeto
  django-admin stratproject django2 .
3. criação aplicação
   django-main startapp core
4. configuração settings.py
 INSTALLED_APPS = [
    'core',
    'bootstrap4',
    'stdimage',
]

MIDDLEWARE = [
    # 'whitenoise.middleware.WhiteNoiseMiddleware',
]
TEMPLATES = [
        'DIRS': ['templates'],
]

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'django2',
        'USER': 'alanisandrade',
        'PASSWORD': '0301',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}

LANGUAGE_CODE = 'pt-br'

TIME_ZONE = 'America/Sao_Paulo'

STATIC_ROOT = os.path.join(BASE_DIR, 'static')
