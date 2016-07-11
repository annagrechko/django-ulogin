Конфигурация проекта
====================

Для подключения к проекту откройте ``settings.py`` и добавьте в кортеж ``INSTALLED_APPS`` приложение ``django_ulogin``

.. code:: python

    INSTALLED_APPS += (
        'django_ulogin', 
    )

Добавьте схему URL-адресов к списку ``urlpatterns`` Вашего проекта (``urls.py``):

.. code:: python

    urlpatterns += patterns('',
        url(r'^ulogin/', include('django_ulogin.urls')),
    )

Затем следует синхронизировать базу данных

.. code:: bash

    $ python manage.py makemigrations
    $ python manage.py migrate

