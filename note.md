# Initialize Laravel 5.3 Project
```
laravel new laravel_5_3_site
```

# Configure project configuration
```
.env
```

# Create database with UTF-8
```
CREATE DATABASE laravel_5_3_site CHARACTER SET utf8 COLLATE utf8_general_ci;
```

# Install BootForm via composer

    ```
    composer require watson/bootstrap-form
    ```

    *   Change config/app.php
    ```
    'providers' => [

        /*
         * BootstrapForm for Laravel
         */
        Collective\Html\HtmlServiceProvider::class,
        Watson\BootstrapForm\BootstrapFormServiceProvider::class,

    ],
    'aliases' => [

        'Form'     => Collective\Html\FormFacade::class,
        'HTML'     => Collective\Html\HtmlFacade::class,
        'BootForm' => Watson\BootstrapForm\Facades\BootstrapForm::class

    ]
    ```

    *   Generate BootForm Configure
    ```
    php artisan vendor:publish
    ```