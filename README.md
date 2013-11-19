Api-php
=======
Version 1.0

Introduction
------------

This repository is a wrapper for the Coursio API, which simplifies the key-generation and communication to the API

Installation
------------

### Main Setup

#### By cloning project

1. Clone this project into your `./vendor/` directory.

#### With composer

1. Add this project in your composer.json:

    ```
        {
            ...
            "name": ...,
            "require": {
                ...
                "coursio/api-php": "1.0.0",
                ...
            }
            ...
        }
    ```

2. Now tell composer to download Api-php by running the command:

    ```bash
    $ php composer.phar update
    ```

Usage
------------

```php
<?php
use Coursio\CoursioApi;

$API = new CoursioApi ("YOUR_PUBLIC_KEY", "YOUR_PRIVATE_KEY", "YOUR_SALT");

$result = $API->Get('courses');
print_r($result);

$result = $API->Post('invitations', array
(
    'courseId' => 65,
));
print_r($result);

```