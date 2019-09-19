
### week1:

- Code editor

Using rich-featured IDE(Integrated Development Environment) or a lighter code editor comes down to personal preferences. I like to use smaller and quicker code editor, and I use Atom.

Atom is available on all platforms, Atom is billed as the “hackable text editor for the 21st Century.” With a sleek interface, file system browser, and my favorite is the marketplace for extensions.

Highly recommend the following extensions/packages to be installed in Atom:
https://atom.io/packages/atom-beautify
  Beautify your python script
https://atom.io/packages/python-autopep8
  Format python code using autopep8
https://atom.io/packages/docblock-python
  Inserts documentation blocks for python functions

- Virtual Environment

Imagine a scenario where you are working on two python projects and one of them uses a Pandas 1.9 and the other uses Pandas 2.0 and so on. In such situations virtual environment can be really useful to maintain dependencies of both the projects. Virtual environment is a tool helps to keep dependencies required by different projects separate by creating isolated python virtual environments for them.

If you are using Python 3, then you should already have the venv module from the standard library installed.

Tutorial of venv: https://realpython.com/python-virtual-environments-a-primer/

### week2: 
- Package your python project -- setup.py

Package your code to share it with other developers and users makes a great impact. Just like how we install packages using pip and PyPI, packaging your project in a well-established distribution convention makes it easy to share.

Setup.py is the build script for setuptools. It tells setuptools about your package (such as the name and version) as well as which code files to include.

setup() takes several arguments.

- name is the distribution name of your package. Choose a memorable and unique name for your package.
- version is the package version see PEP 440 for more details on versions.
author and author_email are used to identify the author of the package.
description is a short, one-sentence summary of the package.
- packages is a list of all Python import packages that should be included in the distribution package. Instead of listing each package manually, we can use find_packages() to automatically discover all packages and subpackages.
- classifiers gives the index and pip some additional metadata about your package, usually including: python version, license, etc.

More read of package python:https://packaging.python.org/tutorials/packaging-projects/

### week3:

### week4 :airflow

1. First installing Airflow
```
pip install apache-airflow[postgres]
pip3 install psycopg2-binary
```
2. Setup Airflow environment variable
Add following line in ~/.bash_profile to set an important environment variable called AIRFLOW_HOME

3. Initialize the database
```
airflow initdb
```
4. start the web server, default port is 8080
```airflow webserver -p 8080
```
5. start the scheduler
```
airflow scheduler
```
then visit localhost:8080 in the browser and enable the example dag in the home page

6.(Optional) 
- Mac user:If using postgress as the sql backend, install postgressapp first, following the 3 steps in this [start-up page](https://postgresapp.com/), then update the following settings in airflow/airflow.cfg file as following:
```
sql_alchemy_conn = postgresql://localhost:5432
executor = LocalExecutor
sql_alchemy_schema = public
```
then restart from step 3 to initialize the db.
- Linux user: follow this [article] (https://medium.com/@taufiq_ibrahim/apache-airflow-installation-on-ubuntu-ddc087482c14)

[Use Airflow to build a Recommender System from end to end on AWS] (https://github.com/aws-samples/sagemaker-ml-workflow-with-apache-airflow)

