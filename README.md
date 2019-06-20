## Introduction

This is a simple Todo application built off Django (including the Django REST Framework for API CRUD operations) and React.

This forked repository has added settings/scripts to allow usage inside Docker.

## Requirements
* Docker installation
* your host requires to be MacOS or Linux to run the helper scripts, otherwise you need to convert them into 'cmd' scripts (easy!)

## Getting started
1. Clone the project to your machine ```[git clone https://github.com/Jordanirabor/django-todo-react]```
2. Navigate into the diretory ```[cd django-todo-react]```
3. Source the virtual environment ```[pipenv shell]```
4. Install the dependencies ```[pipenv install]```
5. Navigate into the frontend directory ```[cd frontend]```
5. Install the dependencies ```[npm install]```

## Run the application
You will need two terminals pointed to the frontend and backend directories to start the servers for this application.

1. Run this command to start the backend server in the ```[backend]``` directory: ```[python manage.py runserver]``` (You have to run this command while you are sourced into the virtual environment)
2. Run this command to start the frontend development server in the ```[frontend]``` directory: ```[npm start]``` (This will start the frontend on the adddress [localhost:3000](http://localhost:3000))

## Run inside docker (the below mentioned scripts easly can be converted into windows scripts, they do not contain Linux/MacOS specific code)
1. Go to docker folder and run the script to build the actual image: ./build_image.sh
2. Go to docker folder and run the docker image that will point to this local folder: ./run_image.sh
3. Now you are logged into the docker container, you can now start the backend as described above. An easier way is to use the start script in the back end folder: ./run_server.sh
4. Now open another shell and attach to docker again to run the frontend: go to the docker folder and call ./attach_image.sh.
5. Go to frontend folder and start node as described above: npm start

## Built With

* [React](https://reactjs.org) - A progressive JavaScript framework.
* [Python](https://www.python.org/) - A programming language that lets you work quickly and integrate systems more effectively.
* [Django](http://djangoproject.org/) - A high-level Python Web framework that encourages rapid development and clean, pragmatic design.