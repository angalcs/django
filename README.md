## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)

## General info
A simple dockerized django project with postgres and nginx.
	
## Technologies
Project is created with:
* Django
* Postgres
* Nginx
* Docker

## Setup
Well we don't use requirements.txt to install pip packages.
Instead we install pipenv and simply use it to install pip packages with 2 simple commands.
First install pipenv using :
```
$ pip install pipenv 
```
Then go to app directory and create a file named pipfile and copy the pipfile text to it :
```
$ cd ./app
```

then just run 
```
$ pipenv lock 
```
and it creates a file named pipfile.lock
after that u can use the pipfile.lock to install the packages using :
```
$ pipenv install --skip-lock --system
```
