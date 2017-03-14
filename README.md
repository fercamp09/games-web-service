# games-web-service
Create venv: python -m venv %USERPROFILE%\PythonREST\Django01
Activate venv %USERPROFILE%\PythonREST\Django01\Scripts\activate.bat
Deactivate venv (%USERPROFILE%\PythonREST\Django01\Scripts\deactivate.bat
pip install django
pip install djangorestframework
cd /d %USERPROFILE%\PythonREST\Django01
"python Scripts/django-admin.py startproject gamesapi" era "django-admin.py startproject gamesapi"
cd gamesapi
python manage.py startapp games
generate migration file: python manage.py makemigrations games
apply migration: python manage.py migrate
interactive shell: python manage.py shell
launch server:python manage.py runserver
curl: curl -iX GET localhost:8000/games/
httpie:http GET localhost:8000/games/
add -b for hidding header

PATCH: update single field
PUT: update all fields
GET: obtain info
POST: create item	
DELETE: delete item

Get options available from the api http OPTIONS :8000/games/ 
pip install psycopg2
python manage.py makemigrations games
python manage.py migrate
DATABASES = {
    'default': { 
        'ENGINE': 'django.db.backends.postgresql', 
        # Replace games with your desired database name 
        'NAME': 'bpyobpqw', 
        # Replace username with your desired user name 
        'USER': 'bpyobpqw', 
        # Replace password with your desired password 
        'PASSWORD': 'WG-948xqCS_JjV-TJfGEaxF0TpK_GJoC', 
        # Replace 127.0.0.1 with the PostgreSQL host 
        'HOST': 'babar.elephantsql.com', 
        # Replace 5432 with the PostgreSQL configured port 
        # in case you aren't using the default port 
        'PORT': '5432', 
    } 
}
