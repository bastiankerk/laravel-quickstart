# laravel-quickstart
Very first steps you need for a MVC structure with database setup.


###### create table:
php artisan make:migration create_users_table<br />
+++ add table fields by hand +++<br />
php artisan migrate<br /><br />

###### initial table:
php artisan make:seeder UsersTableSeeder<br />
+++ add values by hand +++<br />
php artisan db:seed --class=UsersTableSeeder<br /><br />

###### create model for table entries:
php artisan make:model User<br /><br />

###### create controller:
php artisan make:controller UserController<br /><br />

###### Show Funktion anlegen:
    public function show($id)<br />
    {<br />
        return view('users', User::all());<br />
    }<br /><br />

###### create view:
create file by hand in resources/views/users.blade.php<br />
+++ access on users object by $users +++<br /><br />

###### create route:
create entry by hand in routes/web.php<br />
Route::get('users', 'UserController@show');


