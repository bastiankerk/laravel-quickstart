# laravel-quickstart
Very first steps you need for a MVC structure with database setup.


create table:
php artisan make:migration create_users_table
+++ add table fields by hand +++
php artisan migrate

initial table:
php artisan make:seeder UsersTableSeeder
+++ add values by hand +++
php artisan db:seed --class=UsersTableSeeder

create model for table entries:
php artisan make:model User

create controller:
php artisan make:controller UserController

Show Funktion anlegen:
    public function show($id)
    {
        return view('users', User::all());
    }

create view :
create file by hand in resources/views/users.blade.php
+++ access on users object by $users +++

create route:
create entry by hand in routes/web.php
Route::get('users', 'UserController@show');


