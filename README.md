# sso-django
Single Sign On code for Nerdy Python website to allow for authentication to all our other applications/endpoints.  Based initially off Auth0.com example [Auth0 Django Example](https://auth0.com/docs/quickstart/webapp/django/01-login)

# Running the App

To run the application:

1. Make sure you have `python`, `pip` installed.
2. Rename `.env.example` to `.env` and populate it with the client ID, domain, secret.
3. Register `http://localhost:3000/complete/auth0` as `Allowed Callback URLs` and `http://localhost:3000`
as `Allowed Logout URLs` in your app settings.

Once you've set those variables:

1. Install the needed dependencies with `pip install -r requirements.txt`
2. Run `python manage.py migrate` to migrate the database schema
3. Run `python manage.py runserver 3000` to run the server.

The app will be served at [http://localhost:3000/](http://localhost:3000/).

# Running the App with Docker

To run the sample with `docker`:

1. Rename the `.env.example` file to `.env`, change the environment variables, and register the URLs as explained [previously](#running-the-app).
2. Run `sh exec.sh` to build and run the docker image in Linux or run `.\exec.ps1` to build and run the docker image 
on Windows.

The app will be served at [http://localhost:3000/](http://localhost:3000/).

