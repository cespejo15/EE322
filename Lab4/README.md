# Lab 4 #
Lab 4 focused on Django and Flask, involving the installation of packages for these programs and then running some projects. To begin with, I installed Django and Django REST framework on my device. But before i started installing anything, I made sure to initialize a virtual environment:

![venv terminal capture](https://github.com/cespejo15/EE322/blob/main/Lab4/venv.PNG)

After the virtual environment was made, I knew it was safe to start using pip install commands. So, I started installing.

$ pip3 -V outputs the following:
 
 ![pip3](https://github.com/cespejo15/EE322/blob/main/Lab4/-V.PNG)
 
$ pip3 list outputs the following:

![pip3 list](https://github.com/cespejo15/EE322/blob/main/Lab4/list.PNG)

I tried doing sudo pip3 install for the first installation, but sudo did not work since I was on my laptop, so I just used pip install

$ pip3 install -U setuptools outputs the following:

![setuptools](https://github.com/cespejo15/EE322/blob/main/Lab4/setuptools.PNG)

$ pip3 install -U django outputs the following:

![django](https://github.com/cespejo15/EE322/blob/main/Lab4/django.PNG)

$ pip3 install -U djangorestframework outputs the following:

![django rest framework](https://github.com/cespejo15/EE322/blob/main/Lab4/djangorestframework.PNG)

$ pip3 install -U django-filter outputs the following:

![filter](https://github.com/cespejo15/EE322/blob/main/Lab4/djangofilter.PNG)

$ pip3 install -U markdown outputs the following:

![markdown](https://github.com/cespejo15/EE322/blob/main/Lab4/markdown.PNG)

$ pip3 install -U requests outputs the following:

![requests](https://github.com/cespejo15/EE322/blob/main/Lab4/requests.PNG)

After installing these packages, I opened the README.md file from the stevens project, and began starting the stevens Django project.

I first started the Django project:

![startproject](https://github.com/cespejo15/EE322/blob/main/Lab4/startprojectterminal.PNG)

I then started the Django app:

![startapp](https://github.com/cespejo15/EE322/blob/main/Lab4/startapp.PNG)

Afterwards I went into the settings.py file using the nano command:

![nano](https://github.com/cespejo15/EE322/blob/main/Lab4/nano.PNG)

And I changed the file to look like this:

![settings](https://github.com/cespejo15/EE322/blob/main/Lab4/settings2.PNG)

Next, I tried to use the cp command to copy certain files to the stevens and myapp directories, but it was not working, so I just went into my file explorer and manually copied and pasted the desired files into their desired folders.
I then made a templates folder and another myapp folder and copy-pasted the intended files into it:

![templates](https://github.com/cespejo15/EE322/blob/main/Lab4/templatesmyapp.PNG)

Next, I signed up for Google Maps Platform, received an API key, and insert my API key into the index.html file

After this, I copied the favicon.ico file into the static folder. I then copied the .css and .js files into the myapp folder.

Next, I executed the following commands:

$ python manage.py makemigrations myapp

![makemigrations](https://github.com/cespejo15/EE322/blob/main/Lab4/makemigrations.PNG)

$ python manage.py migrate

![migrate](https://github.com/cespejo15/EE322/blob/main/Lab4/migrate.PNG)

$ python manage.py createsuperuser

![createsuperuser](https://github.com/cespejo15/EE322/blob/main/Lab4/createsuperuser.PNG)

After running these commands, I was able to start running the Django server with the following command:

$ python manage.py runserver

This started the server and I was able to navigate to http://127.0.0.1:8000/admin, login with my username and password I created, and entered in to receive the following screen:

![server](https://github.com/cespejo15/EE322/blob/main/Lab4/server2.PNG)

I entered in the following temperature data:

![temperature](https://github.com/cespejo15/EE322/blob/main/Lab4/temperature.PNG)

After hitting save, I was sent to this screen:

![servertemp](https://github.com/cespejo15/EE322/blob/main/Lab4/servertemp.PNG)

Then, I went to the app at http://127.0.0.1:8000 and received the following:

![app](https://github.com/cespejo15/EE322/blob/main/Lab4/app.PNG)
