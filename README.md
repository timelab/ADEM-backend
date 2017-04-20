# ADEM-backend

This backend is a webservice, created using Python, Django and PostGreSQL. 

# Installation
Install Python 2.7 and all its dependencies (see requirements.txt)
Install PostGreSQL
In PostGres create database and user for ademplatform
Create a workdir
add a json-file "django_credentials.json" with following content:
{"hostname":"127.0.0.1",
"port":"5432",
"dbname":"xxxx",  -> name of database
"username":"xxxx",  -> name of PostGresUser
"password":"xxxx",  -> password of PostGresUser
"debug":true,
"static_root":"local path where all static files are collected"}
From this workdir, execute following commands:
>> python ../bin/manage.py makemigrations (-> prepares the creation of databasetables )
>> python ../bin/manage.py migrate (-> creates the databasetables )
>> python ../bin/manage.py createsuperuser (give name, email and password of min. 8 characters)
>> python ../bin/manage.py collectstatic  (-> collects static files to the local path, this local path needs to be accessible for the webserver, see further)

To test the testserver, execute following command
>> python ../bin/manage.py runserver

Now test on http://IPadres:8000/ademplatform/