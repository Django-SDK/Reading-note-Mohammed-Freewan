Databases: 


Django officially supports the following databases:

PostgreSQL
MariaDB
MySQL
Oracle
SQLite
There are also a number of database backends provided by third parties.

Django attempts to support as many features as possible on all database backends. However, not all database backends are alike, and we’ve had to make design decisions on which features to support and which assumptions we can make safely.

This file describes some of the features that might be relevant to Django usage. It is not intended as a replacement for server-specific documentation or reference manuals.


PostgreSQL notes¶


Django supports PostgreSQL 11 and higher. psycopg2 2.8.4 or higher is required, though the latest release is recommended.

PostgreSQL connection settings¶
See HOST for details.

To connect using a service name from the connection service file and a password from the password file, you must specify them in the OPTIONS part of your database configuration in DATABASES:

settings.py: 

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'OPTIONS': {
            'service': 'my_service',
            'passfile': '.my_pgpass',
        },
    }
}
.pg_service.conf: 


        [my_service]
        host=localhost
        user=USER
        dbname=NAME
        port=5432
        .my_pgpass¶
        localhost:5432:NAME:USER:PASSWORD
Changed in Django 4.0:
Support for connecting by a service name, and specifying a password file was added.



