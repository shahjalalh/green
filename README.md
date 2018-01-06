# green: A Green Solution

[<img src="https://img.shields.io/badge/built%20with-Cookiecutter%20Django-ff69b4.svg">](https://github.com/pydanny/cookiecutter-django/)


## License: MIT


## Settings:

[Moved to settings][Moved to settings]


## Basic Commands:


### Setting Up Your Users

* To create a **normal user account**, just go to Sign Up and fill out the form. Once you submit it, you'll see a "Verify Your E-mail Address" page. Go to your console to see a simulated email verification message. Copy the link into your browser. Now the user's email should be verified and ready to go.

* To create an **superuser account**, use this command::
```
$ python manage.py createsuperuser
```
For convenience, you can keep your normal user logged in on Chrome and your superuser logged in on Firefox (or similar), so that you can see how the site behaves for both kinds of users.


### Test coverage

To run the tests, check your test coverage, and generate an HTML coverage report::

```
$ coverage run manage.py test
$ coverage html
$ open htmlcov/index.html
```


### Running tests with py.test

```
$ py.test
```


### Live reloading and Sass CSS compilation

Moved to [Live reloading and SASS compilation][Live reloading and SASS compilation]


### Celery

This app comes with Celery.

To run a celery worker:

```
cd green
celery -A green.taskapp worker -l info
```

**Please note:** For Celery's import magic to work, it is important *where* the celery commands are run. If you are in the same folder with *manage.py*, you should be right.


## Email Server

In development, it is often nice to be able to see emails that are being sent from your application. For that reason local SMTP server [MailHog][MailHog] with a web interface is available as docker container.

Container mailhog will start automatically when you will run all docker containers.
Please check [cookiecutter-django Docker documentation][cookiecutter-django Docker documentation] for more details how to start all containers.

With MailHog running, to view messages that are sent by your application, open your browser and go to 
```
http://127.0.0.1:8025
```

MailHog GitHub:[https://github.com/mailhog/MailHog][MailHog]


## Deployment

The following details how to deploy this application.


### Heroku

See detailed [cookiecutter-django Heroku documentation][cookiecutter-django Heroku documentation]


### Docker

See detailed [cookiecutter-django Docker documentation][cookiecutter-django Docker documentation]


[Moved to settings]: http://cookiecutter-django.readthedocs.io/en/latest/settings.html
[Live reloading and SASS compilation]: http://cookiecutter-django.readthedocs.io/en/latest/live-reloading-and-sass-compilation.html
[MailHog]: https://github.com/mailhog/MailHog
[cookiecutter-django Docker documentation]: http://cookiecutter-django.readthedocs.io/en/latest/deployment-with-docker.html
[cookiecutter-django Heroku documentation]: http://cookiecutter-django.readthedocs.io/en/latest/deployment-on-heroku.html
[cookiecutter-django Docker documentation]: http://cookiecutter-django.readthedocs.io/en/latest/deployment-with-docker.html
