
# Description
Self project to learn Django backend by creating a hospital management system

# Requirements
See requirements.txt

# Running Locally
1) In the .env file, make sure 'DB_HOST' is set to 'localhost'
2) Run the activate.bat file
3) Create a superuser by typing 'python mangae.py createsuperuser'
4) In the terminal type 'python manage.py runserver
5) Enter '127.0.0.1:8000' in address bar

# Running on Docker
1) In the .env file, make sure 'DB_HOST' is set to 'db' (to reference the db created in docker-compose.yml)
2) Run the activate.bat file
3) Create the containers by typing "docker compose build"
4) Create the superuser for the docker container by typing "docker compose run <name of service in docker-compose.yaml, here use 'web'> python manage.py createsuperuser"
5) Run the containers by typing "docker compose up -d"

# Features
1) 127.0.0.1:8000/admin           -Admin panel to manage the database via the web
2) 127.0.0.1:8000/Doctors         -List view of all the doctors
3) 127.0.0.1:8000/Doctors/<pk>    -Detail view of the doctor, allows staff users to edit/delete an existing doctor
4) 127.0.0.1:8000/Doctors/create  -Create view to add a new doctor
5) 127.0.0.1:8000/api             -View available API's 

# Notes
1) If makemigration isn't detecting the models, try typing "python manage.py makemigrations <name of project, here use 'myapp'>
2) It is bad practice to load the .env file into the docker container, but we are not using a secret manager so .dockerignore does not exclude .env
