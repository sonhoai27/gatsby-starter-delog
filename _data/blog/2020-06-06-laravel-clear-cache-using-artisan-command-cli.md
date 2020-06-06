---
template: BlogPost
path: /php-clear-cache
date: 2020-06-06T18:48:13.160Z
title: Laravel Clear Cache Using Artisan Command (CLI)
metaDescription: >-
  Simply clear cache from the command line (CLI), In this laravel tutorial, we
  will discuss how to clear cache from blade (views), routes, config, etc using
  the command line and artisan command.
thumbnail: /assets/laravel-clear-cache-artisan-command.jpeg
---
When our app is product mode (live), we need to make cache in larva projects for better completion. But if our application is development mode then what we want to do is not get cured due to the cache. At this time we need to clear the cache.

### List of the cache clear commands, see below

#### Clear Route Cache

Use the below command and clear your routes cache :

```
php artisan route:cache
```

#### Clear Cache Laravel Application

Use the below command and clear your application cache :

```
php artisan cache:clear
```

#### Laravel Clear Config Cache

Use the below command and clear your config cache :

```
php artisan config:cache
```

#### Clear View Cache Laravel

Use the below command and clear your view (blade) cache :

```
php artisan view:clear
```

#### Reoptimized Class

```
php artisan optimize
```

We do not access SSH on shared hosting servers, then we can also clear the cache by typing the code in route file. Go to your web.php file and put below code for clear cache of your application :

```php
//Clear route cache:
 Route::get('/route-cache', function() {
     $exitCode = Artisan::call('route:cache');
     return 'Routes cache cleared';
 });

 //Clear config cache:
 Route::get('/config-cache', function() {
     $exitCode = Artisan::call('config:cache');
     return 'Config cache cleared';
 }); 

// Clear application cache:
 Route::get('/clear-cache', function() {
     $exitCode = Artisan::call('cache:clear');
     return 'Application cache cleared';
 });

 // Clear view cache:
 Route::get('/view-clear', function() {
     $exitCode = Artisan::call('view:clear');
     return 'View cache cleared';
 });
```
