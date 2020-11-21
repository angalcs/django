# django
a simple django docker with postgres and nginx

Well we don't use requirements.txt to install pip packages.
Instead we install pipenv and simply use it to install pip packages with 2 simple commands.
First install pipenv using : pip install pipenv , Then go to /app directory and create a file named pipfile and type the things below :
##
[[source]]

url = "https://pypi.python.org/simple"
verify_ssl = true
name = "pypi"


[packages]

django = "*"
gunicorn = "*"
psycopg2 ="*"

[dev-packages]

tox = "*"
ipython = "*"

[requires]

python_version = "3.9"
##
then just run pipenv lock and it creates a file named pipfile.lock
after that u can use the pipfile.lock to install the packages using : pipenv install --skip-lock --system
