# Django Chat Application

This is a real-time chat application built using Django, Channels, and Daphne.

## Installation

1. Install Django:

   ```bash
   pip install django

2.Create a Django project:
  ```bash
  django-admin startproject myproject

3.Install Channels and Daphne:
  ```bash
  pip install channels daphne

##Why ASGI, Daphne, and Channels?
ASGI (Asynchronous Server Gateway Interface) is necessary for handling asynchronous tasks, such as WebSockets, in Django. Daphne is an ASGI server used to run Django applications with Channels, which allows for real-time features like chat.

Setup
Add 'channels' and 'daphne' to your INSTALLED_APPS in settings.py.
Set the ASGI application in settings.py:
  ```bash
  ASGI_APPLICATION = 'myproject.asgi.application'

Create a new Django app for the chat functionality:
  ```bash
  python manage.py startapp chat

Specify the URLs in urls.py to route to the chat app.
Create a templates directory in the chat app for the login page and chat page HTML templates.
Design
You can design the login page and chat page as you wish using HTML and CSS.

Database Migration
Before running the application, make sure to create and apply migrations:
  ```bash
  python manage.py makemigrations
  python manage.py migrate

Migrations are necessary to create database tables for storing user information and chat messages.

Creating Users
To create two users, use the following command:
  ```bash
  python manage.py createsuperuser  

Run the server:
  ```bash
  python manage.py runserver

Acknowledgement
This project was developed with the help of GeeksforGeeks.
