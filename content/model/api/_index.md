---
title: "Model APIs"

draft: false
---

# Running the API

**DB creation**

PostgreSQL needs to be installed. To facilitate the configuration, I suggest to use a Db manager with UI, like [pgAdmin](https://www.pgadmin.org/). 

After the installation of PostgreSQL, it is possible to use pgAdmin to create a ```django-emotion-classification``` database and a ```App_filemodel``` table.

The ```App_filemodel``` table can be created with the following script:

```
CREATE DATABASE django-emotion-classification;

CREATE USER marco WITH PASSWORD 'test';

CREATE TABLE App_filemodel (
   id INT PRIMARY KEY NOT NULL,
   file TEXT NOT NULL,
   timestamp DATE NOT NULL,
   path TEXT NOT NULL
);

GRANT SELECT, INSERT, UPDATE, DELETE ON ALL TABLES IN SCHEMA django-emotion-classification TO marco;

ALTER USER marco CREATEDB; -- This is to run the automatic tests, otherwise you will get an "unable to create database" error when running python manage.py test

```

Please note the above script is made with the data available in the ```settings.py```, but it is possible to change it if needed.
```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'django-emotion-classification',
        'USER': 'marco',
        'PASSWORD': 'test',
        'HOST': 'localhost',
        'PORT': '',
        'OPTIONS': {'sslmode': 'disable'},
    }
}
```

**How to start the server and try it**

1) ```git clone https://github.com/Angaza-Elimu/learning_recommendation```
2) ```$ pip install -r requirements.txt```
3) Open a terminal window, ```cd``` into the project folder and run ```python manage.py runserver```.

