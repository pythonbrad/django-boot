# Lithium: A Django-Powered Boilerplate
Lithium is a batteries-included Django starter project with everything you need to start coding, including user authentication, static files, default styling, debugging, DRY forms, custom error pages, and more.

> This project was formerly known as _DjangoX_ but was renamed to _Lithium_ in November 2024.

![Homepage](homepage_41.png)

## 🚀 Features
- Django 5.1 & Python 3.13
- Installation via [uv](https://github.com/astral-sh/uv), [Pip](https://pypi.org/project/pip/) or [Docker](https://www.docker.com/)
- User authentication--log in, sign up, password reset--via [django-allauth](https://github.com/pennersr/django-allauth)
- Static files configured with [Whitenoise](http://whitenoise.evans.io/en/stable/index.html)
- Styling with [Bulma CSS](https://bulma.io/)
- Debugging with [django-debug-toolbar](https://github.com/jazzband/django-debug-toolbar)
- DRY forms with [django-crispy-forms](https://github.com/django-crispy-forms/django-crispy-forms)
- Maintenance Mode [django-maintenance-mode](https://pypi.org/project/django-maintenance-mode/)
- Custom 404, 500, and 403 error pages

## Table of Contents
* **[Installation](#installation)**
  * [uv](#uv)
  * [Pip](#pip)
  * [Pipenv](#pipenv)
  * [Maintenance mode](#maintenance-mode)
  * [Docker](#docker)
* [Next Steps](#next-steps)
* [Contributing](#contributing)
* [Support](#support)
* [License](#license)

## 📖 Installation
DjangoBoot can be installed via Pip, Pipenv, or Docker. To start, clone the repo to your local computer and change into the proper directory.
*NB:* We provide the [raw version](requirements_raw.txt) of the requirements.txt file.

```
$ git clone https://github.com/pythonbrad/django-boot.git
$ cd django-boot
```

### uv
You can use [uv](https://docs.astral.sh/uv/) to create a dedicated virtual environment.

```
$ uv sync
```

Then run `migrate` to configure the initial database. The command `createsuperuser` will create a new superuser account for accessing the admin. Execute the `runserver` command to start up the local server.

```
$ uv run manage.py migrate
$ uv run manage.py createsuperuser
$ uv run manage.py runserver
# Load the site at http://127.0.0.1:8000 or http://127.0.0.1:8000/admin for the admin
```

### Pip
To use Pip, create a new virtual environment and then install all packages hosted in `requirements.txt`. Run `migrate` to configure the initial database. and `createsuperuser` to create a new superuser account for accessing the admin. Execute the `runserver` command to start up the local server.

```
(.venv) $ pip install -r requirements.txt
(.venv) $ python manage.py migrate
(.venv) $ python manage.py createsuperuser
(.venv) $ python manage.py runserver
# Load the site at http://127.0.0.1:8000 or http://127.0.0.1:8000/admin for the admin
```

### Environ

Duplicate the .env_example file in .env and configure your Django application.

### Maintenance mode

```
python ./manage.py maintenance_mode <on|off>
```

### Docker

To build the Docker image, run the container, and execute the standard commands within Docker.

```
$ docker compose up -d --build
$ docker compose exec web python manage.py migrate
$ docker compose exec web python manage.py createsuperuser
# Load the site at http://127.0.0.1:8000 or http://127.0.0.1:8000/admin for the admin
```

## Next Steps

- Add [gunicorn](https://pypi.org/project/gunicorn/) as the production web server.
- Update the [EMAIL_BACKEND](https://docs.djangoproject.com/en/4.0/topics/email/#module-django.core.mail) and connect with a mail provider.
- Make the [admin more secure](https://opensource.com/article/18/1/10-tips-making-django-admin-more-secure).
- `django-allauth` supports [social authentication](https://django-allauth.readthedocs.io/en/latest/providers.html) if you need that.

I cover all of these steps in tutorials and premium courses over at [LearnDjango.com](https://learndjango.com).

## 🤝 Contributing

Contributions, issues and feature requests are welcome! See [CONTRIBUTING.md](https://github.com/pythonbrad/django-boot/blob/master/CONTRIBUTING.md).

## ⭐️ Support

Give a ⭐️  if this project helped you!

## License

[The MIT License](LICENSE)
