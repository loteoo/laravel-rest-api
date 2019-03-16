# laravel-rest-api
CTRL web presentation


## Steps

1. Setup DB + migrate:  
```
php artisan migrate
```


2. Seed DB:  
`database\seeds\DatabaseSeeder.php`
```
factory(App\User::class, 50)->create();
```
and run `php artisan db:seed`


3. Generate controller:  
`php artisan make:controller Api/UserController --api`  


4. Setup REST API routing
`routes\api.php`
```
Route::apiResource('users', 'Api\UserController');
```


5. Implement business logic:  
`app\Http\Controllers\Api\UserController.php`

Import Model:  
```
use App\User;
```
