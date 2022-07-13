<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

Installation Steps

1. Require the Package
After creating your new Laravel application you can include the Voyager package with the following command:

**composer require tcg/voyager**

2. Add the DB Credentials & APP_URL

Next make sure to create a new database and add your database credentials to your .env file:

**DB_HOST=localhost
DB_DATABASE=homestead
DB_USERNAME=homestead
DB_PASSWORD=secret**

You will also want to update your website URL inside of the APP_URL variable inside the .env file:

**APP_URL=http://localhost:8000**

3. Run The Installer
Lastly, we can install voyager. You can do this either with or without dummy data. The dummy data will include 1 admin account (if no users already exists), 1 demo page, 4 demo posts, 2 categories and 7 settings.

To install Voyager without dummy simply run

**php artisan voyager:install**

If you prefer installing it with dummy run

**php artisan voyager:install --with-dummy**

And we're all good to go!

Start up a local development server with php artisan serve And, visit **http://localhost:8000/admin.**

Creating an Admin User

If you did go ahead with the dummy data, a user should have been created for you with the following login credentials:
**
email: admin@admin.com
password: password**

NOTE: Please note that a dummy user is only created if there are no current users in your database.

If you did not go with the dummy user, you may wish to assign admin privileges to an existing user. This can easily be done by running this command:

**php artisan voyager:admin your@email.com**

If you did not install the dummy data and you wish to create a new admin user, you can pass the --create flag, like so:

**php artisan voyager:admin your@email.com --create**

And you will be prompted for the user's name and password.
