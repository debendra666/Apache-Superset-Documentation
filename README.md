# Apache-Superset-Documentation
Having our analytics in a streaming fashion enable us to continuously analyze our  customer's behaviour and immediately take action on it.
Apache™ Superset is a data exploration and visualization web application and provides an intuitive interface to explore and visualize datasets, and create interactive dashboards. Initially developed by Airbnb, but now in the running to become an Apache™ project.
#Installation Guide(Linux Based)
Here, how to install them
For Debian and Ubuntu, the following command will ensure that the required dependencies are installed:
sudo apt-get install build-essential libssl-dev libffi-dev python-dev python-pip libsasl2-dev libldap2-dev

# Note : otherwhise build for cryptography fails.

Ubuntu 16.04 If you have python3.5 installed alongside with python2.7, as is default on Ubuntu 16.04 LTS, run this command also:
sudo apt-get install build-essential libssl-dev libffi-dev python3.5-dev python-pip libsasl2-dev libldap2-dev

# Python virtualenv
pip install virtualenv
For creating  and activating virtual environment
virtualenv venv
. ./venv/bin/activate
# Note : upgrade to python3 inside the virtual enviroment if it shows python2

# Python’s setup tools and pip
pip install --upgrade setuptools pip

# Superset installation and initialization
pip install superset

# Create an admin user (you will be prompted to set username, first and last name before setting a password)
fabmanager create-admin --app superset

# Initialize the database
superset db upgrade

# Load some data to play with
superset load_examples

# Create default roles and permissions
superset init

To start a development web server on port 8088, use -p to bind to another port
superset runserver -d
# Note : If it shows error while connnecting to the local host then try to connect to another new port as like
superset runserver -p 9000

