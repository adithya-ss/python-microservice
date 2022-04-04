# python-microservice
Python Microservices Web App (with React, Django, Flask) - Source: freeCodeCamp

Monolith
    - Large code base with lot of functionalities. Connected with single big database.
    - Scalability is difficult. Replication needs to happen at all layers/functionalities, during a change or an update.

Microservices 
    - Smaller indepedant services having their own database. Can communicate with each other using an event bus.
    - These are independantly scalable. Different programming languages can be used based on the need.

Important Docker Commands:
    docker-compose up
    docker-compose exec backend sh
    python manage.py makemigrations
    python manage.py migrate

Important Django Commands:
    django-admin startproject admin
    python manage.py startapp products

To create tables in MySQL, we have to create models and run migrations. This is done in <app_name>/models.py
Migrations are stored in a python file, auto generated whose id will be auto incremented. Ex: 0001_initial.py

Object returned through serializers.

CRUD operations are defined inside views.py
    - list, create, retrive, update, destroy.
    - All these methods are mapped to thier respective request types inside urls.py for that perticular app, with the end point (path)

For the app's urls/APIs to be reachable/available, they have to also be specified in admin/urls.py