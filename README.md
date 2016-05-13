[![Latest Stable Version](https://poser.pugx.org/benjamincrozat/laravel-dropbox-driver/v/stable)](https://packagist.org/packages/benjamincrozat/laravel-dropbox-driver)
[![License](https://poser.pugx.org/benjamincrozat/laravel-dropbox-driver/license)](https://packagist.org/packages/benjamincrozat/laravel-dropbox-driver)
[![Build Status](https://travis-ci.org/benjamincrozat/laravel-dropbox-driver.svg?branch=master)](https://travis-ci.org/benjamincrozat/laravel-dropbox-driver)
[![Total Downloads](https://poser.pugx.org/benjamincrozat/laravel-dropbox-driver/downloads)](https://packagist.org/packages/benjamincrozat/laravel-dropbox-driver)

# Laravel Dropbox Driver

Dropbox driver for Laravel.

## Installation

```php
composer require benjamincrozat/laravel-dropbox-driver
```

## Usage

In your ```config/app.php```, add the service provider:

```php
'providers' => [

    BC\LaravelDropboxDriver\ServiceProvider::class,

],
```

Next, add the following in ```app/filesystems.php```:
```php
'disks' => [

    'dropbox' => [
        'driver' => 'dropbox',
        'app_secret' => env('DROPBOX_APP_SECRET'),
        'token' => env('DROPBOX_TOKEN'),
    ],

],
```

Then, in your ```.env``` file:
```
DROPBOX_APP_SECRET=your_app_secret_key
DROPBOX_TOKEN=your_access_token
```

**Dealing with Dropbox for the first time? Here's the [link](https://www.dropbox.com/developers/apps/create) to create your first application and generate your app secret key and access token.**

## License

[WTFPL](http://www.wtfpl.net/about/)