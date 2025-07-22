# CapStone
DjangoProj

# Description
DJango project to learn fullstack dev cycle a python dev by simulating a hospital management system

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

# Notes
1) If makemigration isn't detecting the models, try typing "python manage.py makemigrations <name of project, here use 'myapp'>
2) It is bad practice to load the .env file into the docker container, but we are not using a secret manager so .dockerignore does not exclude .env
