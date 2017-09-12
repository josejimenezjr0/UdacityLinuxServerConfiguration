# Udacity Linux Server Configuration

I will take a baseline installation of a Linux distribution on a virtual machine and prepare it to host my web applications, to include installing updates, securing it from a number of attack vectors and installing/configuring web and database servers.

## Access information

- Public IP: `52.14.133.246`
- SSH Port: `2200`
- Wed App URL: http://52.14.133.246/

## Installed Software

The server came with a base Ubuntu image. The main aplication I installed were PostgreSQL, Apache, and Python
- PostgreSQL: This was to serve the database information for the Item Catalog web app.
- Python: The Python language along with all the Python dependencies for the web app.
- Apache: This is the web server for the python app.
- WSGI: for the interface between web servers and web apps for python.

## Configurations Made

### Ubuntu
- Set password: I changed the default passwords to the accoutns
- Update packages: I updated all the available packages with apt-get update
- Created a user: I made a user named grader
- Gave grader user sudo: I modified the sudoers files to promote the grader user to sudo access
- Remove root access: I turned off access to the root user
- remove password access: I forced access to all accounts to be only through key based access
- PKI setup: I created SHA keys that allowed access to the users
- Configure firewall: I configured the simple firewall to only allow access to the 2200, 80, and 123 ports

### Postgres
- Add user in Postgres: After installing Postgres I had to make a database user named grader and I gave them access to the database
- create database: I created a new Item Catalog database
- run initial setup: I ran the initial python scripts to create the tables and fill in the database

### Apache
- Installed and enabled mod-wsgi
- made virtual environment for Flask and directory structure for python app
- configured a virtual host by creating a .conf file and adding in my server info and app directory sturcture
- created a .wsgi file and configured it for my web app

## Third-Party Resources

### Amazon Lightsail
I use Amazon Lightsail to host my virtual machine server. I configured Lightsail by creating an instance of an Ubuntu image that had only the OS and some basic built-in applications. I started the machine up and SSH in to configure it. I modified the firewall from the Lightsail site to allow for a differnt port for SSH.

### Python dependencies
- Flask
- SQLAlchemy




