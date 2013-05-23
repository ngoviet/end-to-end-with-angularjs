end-to-end-with-angularjs
==================

[Screencast published May 21, 2013](http://www.youtube.com/watch?v=hqAyiqUs93c)

This is an extension of my screencast ["Intro to Angular JS"](http://www.youtube.com/watch?v=8ILQOFAgaXE) that focuses more on intermediate/advanced topics and walks through creating a working web application on top of the Laravel 4 Web Application Framework. Things you can expect to learn by watching the screencast:

* $http
* $rootScope
* taking the [AuthenticationService](https://github.com/davemo/intro-to-angularjs/blob/master/app/js/app.js#L19) we built earlier end-to-end
* creating a FlashService for displaying alerts to users
* access control for client-side routes with $rootScope and $routeProvider
* $httpProvider.responseInterceptors and logging out users automatically if serverside sessions expire
* $routeProvider.resolve property and making view rendering data dependent
* laravel 4 migrations, controllers, models, and authentication

## Requirements:

* [Laravel 4](http://four.laravel.com/)
* PHP 5.4 or higher
* MCrypt
* MySQL or SQLite
* [AngularJS 1.1.4](https://ajax.googleapis.com/ajax/libs/angularjs/1.1.4/angular.js)

## Prerequisite Installation Instructions:

Installing PHP 5.4 and MCrypt is the most tedious part of getting up and running with this example, but Laravel 4 is so nice that I think it's worth it. Here's the basic instructions for getting up on Mac OS X:

1. Install [Homebrew](http://mxcl.github.io/homebrew/)
2. Make sure you correct any problems that `brew doctor` detects
3. Install [Laravel 4](http://four.laravel.com/#install-laravel)
4. Tap the PHP keg from @josegonzalez: `brew tap josegonzalez/homebrew-php`
5. Install PHP 5.4 `brew install php54`
6. Install MCrypt `brew install php54-mcrypt` (this will automatically link the binary into the php.ini for you)
7. Install [Composer](http://getcomposer.org/) (think of it like homebrew, or npm, or apt-get, but for PHP modules)

## App Installation Instructions:

1. clone this repo: `git clone https://github.com/davemo/end-to-end-with-angularjs.git`
2. install composer dependencies `composer install`
3. create a database called `laravelapp`
4. create your unique security key `php artisan key:generate`
5. create the sessions migration `php artisan session:table`
6. run database migrations `php artisan migrate`
7. seed the database `php artisan db:seed`
8. run the app `php artisan serve`
9. browse to `http://localhost:8000` and log in with email `admin@example.org` and password `admin`

Once you have the app up and running you can visit `http://localhost:8000` and you will see the Login Form.

If you liked this code and screencast you should follow me on twitter: [@dmosher](http://www.twitter.com/dmosher)

Happy Coding! :)
