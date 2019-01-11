# laravel-quickstart
Very first steps you need for a MVC structure with database setup.


create table:<br />
php artisan make:migration create_users_table<br />
+++ add table fields by hand +++<br />
php artisan migrate<br /><br />

initial table:<br />
php artisan make:seeder UsersTableSeeder<br />
+++ add values by hand +++<br />
php artisan db:seed --class=UsersTableSeeder<br /><br />

create model for table entries:<br />
php artisan make:model User<br /><br />

create controller:<br />
php artisan make:controller UserController<br /><br />

Show Funktion anlegen:<br />
    public function show($id)<br />
    {<br />
        return view('users', User::all());<br />
    }<br /><br />

create view :<br />
create file by hand in resources/views/users.blade.php<br />
+++ access on users object by $users +++<br /><br />

create route:<br />
create entry by hand in routes/web.php<br />
Route::get('users', 'UserController@show');


