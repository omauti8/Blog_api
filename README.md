# Blog_api
A simple Django REST framework application to manage blog posts, with token-based authentication (JWT) and role-based access for users. This project allows users to create, read, update, and delete blog posts. Only the author of a post can edit or delete it.

This project is designed to provide a backend for a blog application with user authentication and RESTful APIs. It uses Django, Django REST Framework (DRF), PostgreSQL, and JWT for secure authentication.

git clone https://github.com/omauti8/blog-api.git
cd blog-api

Set Up Virtual Environment
>>python3 -m venv venv

Install the required Python packages:
>>pip install -r requirements.txt

Set Up PostgreSQL
>>sudo -u postgres psql

# Create the database and user
CREATE DATABASE blogdb;
CREATE USER your_username WITH PASSWORD 'your_password';
GRANT ALL PRIVILEGES ON DATABASE blogdb TO your_username;

Update settings.py
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'blogdb',  # The name of your database
        'USER': 'your_username',  # Your PostgreSQL username
        'PASSWORD': 'your_password',  # Your PostgreSQL password
        'HOST': 'localhost',  # Default host
        'PORT': '5432',  # Default PostgreSQL port
    }
}

 Migrate Database
>> python manage.py migrate

Start the Development Server
>> python manage.py runserver

