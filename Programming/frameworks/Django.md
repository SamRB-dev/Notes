- Install django on venv
```shell
python -m venv django
source django/bin/activate
pip install django
```

- Create django project
```shell
django-admin startapp app 
or
django-admin startproject app
```

- Run server
```shell
python manage.py runserver
```

- Send http response
```python
from django.http import HttpResponse
```

- User info collection
```python
dict = request.META 
keys = [
		'REMOTE_ADDR',
		'HTTP_USER_AGENT'
]
```

- Add templates [settings.py]
```python
TEMPLATES = [

{

'BACKEND': 'django.template.backends.django.DjangoTemplates',

'DIRS': ['templates'],

'APP_DIRS': True,

'OPTIONS': {

'context_processors': [

'django.template.context_processors.debug',

'django.template.context_processors.request',

'django.contrib.auth.context_processors.auth',

'django.contrib.messages.context_processors.messages',

			],

		},

	},

]
```

- Add static files [settings.py]
```python
STATIC_URL = 'static/'
STATICFILES_DIRS = [
   os.path.join(BASE_DIR, 'static')
]
```


- Create model / db
```python

```

