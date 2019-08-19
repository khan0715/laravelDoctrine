# Laravel Doctrine 5.4* - How to install doctrine in Laravel

## Getting Started

[How to install 5.4* laravel](https://stackoverflow.com/questions/41838979/how-to-install-laravel-5-4) - Link
[How to install doctrine in Laravel](https://www.laraveldoctrine.org/) - Link 



### Installing
Install this package with composer:

```
composer require "laravel-doctrine/orm:1.3.*"
```

After updating composer, add the ServiceProvider to the providers array in config/app.php


```
LaravelDoctrine\ORM\DoctrineServiceProvider::class,

```

Optionally you can register the EntityManager, Registry and/or Doctrine facade:

```
'EntityManager' => LaravelDoctrine\ORM\Facades\EntityManager::class,
'Registry'      => LaravelDoctrine\ORM\Facades\Registry::class,
'Doctrine'      => LaravelDoctrine\ORM\Facades\Doctrine::class,
```
To publish the config use:

```
php artisan vendor:publish --tag="config"
```


## Extensions (Gedmo)

Install this package with composer:
```
composer require "laravel-doctrine/extensions:1.0.*"
```

This package wraps extensions from Gedmo and Berberlei.

To include Gedmo extensions install them:
```
composer require "gedmo/doctrine-extensions=^2.4"
```
If you are using an annotation driver, then add the Gedmo (Behavioral) extensions service provider in config/app.php:
```
LaravelDoctrine\Extensions\GedmoExtensionsServiceProvider::class,
```
To include Beberlei (Query/Type) extensions install them:
```
composer require "beberlei/DoctrineExtensions=^1.0"
```
And then add the Berberlei extensions service provider in config/app.php:
```
LaravelDoctrine\Extensions\BeberleiExtensionsServiceProvider::class,
```
## Migrations

```
composer require "laravel-doctrine/migrations"
```

After updating composer, add the ServiceProvider to the providers array in config/app.php

```
LaravelDoctrine\Migrations\MigrationsServiceProvider::class,
```

To publish the config use:

```
php artisan vendor:publish --tag="config"
```

## Fluent

```
composer require laravel-doctrine/fluent

```

## ACL

```
composer require "laravel-doctrine/acl:1.0.*"
```

After updating composer, add the ServiceProvider to the providers array in config/app.php

```
LaravelDoctrine\ACL\AclServiceProvider::class,
```

To publish the config use:

```
php artisan vendor:publish --tag="config"
```



