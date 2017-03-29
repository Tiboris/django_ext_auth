Description of setup: https://www.adelton.com/django/external-authentication-for-django-projects

Quick start
-----------
Use new PersistentRemoteUserMiddleware in Django 1.9.
A drop-in replacement for RemoteUserMiddleware:

    MIDDLEWARE = [
        ...
        'django.contrib.auth.middleware.AuthenticationMiddleware',
        'django.contrib.auth.middleware.PersistentRemoteUserMiddleware',
      + 'auth.external.RemoteUserAttrMiddleware',
        ...
    ]

To keep the user authenticated.
