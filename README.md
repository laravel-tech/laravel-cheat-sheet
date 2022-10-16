
# laravel-cheat-sheet
The Laravel cheat sheet intends to provide tips to developers building Laravel applications.

## Requirements
- PHP version >= 7.3
- BCMath PHP Extension
- Ctype PHP Extension
- Fileinfo PHP Extension
- JSON PHP Extension
- Mbstring PHP Extension
- OpenSSL PHP Extension
- PDO PHP Extension
- Tokenizer PHP Extension
- XML PHP Extension

## Composer
> Composer is a tool for dependency management in PHP. It allows you to declare the libraries your project depends on and it will manage (install/update) them for you.

Create new laravel project using composer<br>
`composer create-project laravel/laravel folder_name`

Composer install will install the dependencies into the vendor directory as specified in the composer.lock file.<br>
`composer install`

will update your dependencies as they are specified in `composer.json`<br>
`composer update`

It just regenerates the list of all classes that need to be included in the project.<br>
`composer dump-autoload [--optimize]`

It will update composer.<br>
`composer self-update`

Add new package to the project.<br>
`composer require [options] [--] [vender/packages]...`

Install laravel installer globally.<br>
`composer global require laravel/installer`

Install laravel using laravel installer.<br>
`Laravel new project`

Create .env from .env.example.<br>
`cp .env.example .env`

## Artisan
> _Artisan_ is the command line interface included with _Laravel_.

`php artisan command [options] [arguments]`

Usage:  
command [options] [arguments]
### Options
|Command|Description|
|--|--|
|-h, --help|Display help for the given command. When no command is given|
||display help for the list command|
|-q, --quiet|Do not output any message|
|-V, --version|Display this application version|
|--ansi|--no-ansi|Force (or disable --no-ansi) ANSI output|
|-n, --no-interaction|Do not ask any interactive question|
|--env[=ENV]|The environment the command should run under|
|-v\|vv\|vvv, --verbose|Increase the verbosity of messages: 1 for normal output, 2 for more verbose output and 3 for debug|

### General commands:
|Command|Description|
|--|--|
|about|Display basic information about your application|
|clear-compiled|Remove the compiled class file|
|completion|Dump the shell completion script|
|db|Start a new database CLI session|
|docs|Access the Laravel documentation|
|down|Put the application into maintenance / demo mode|
|env|Display the current framework environment|
|help|Display help for a command|
|inspire|Display an inspiring quote|
|list|List commands|
|migrate|Run the database migrations|
|optimize|Cache the framework bootstrap files|
|serve|Serve the application on the PHP development server|
|test|Run the application tests|
|tinker|Interact with your application|
|up|Bring the application out of maintenance mode|

**auth**<br>
`auth:clear-resets` Flush expired password reset tokens<br>

**cache**<br>
`cache:clear` Flush the application cache<br>
`cache:forget` Remove an item from the cache<br>
`cache:table` Create a migration for the cache database table<br>

**config**<br>
`config:cache` Create a cache file for faster configuration loading<br>
`config:clear` Remove the configuration cache file<br>

**db**<br>
`db:monitor` Monitor the number of connections on the specified database<br>
`db:seed` Seed the database with records<br>
`db:show` Display information about the given database<br>
`db:table` Display information about the given database table<br>
`db:wipe` Drop all tables, views, and types<br>

**env**<br>
`env:decrypt` Decrypt an environment file<br>
`env:encrypt` Encrypt an environment file<br>

**event**<br>
`event:cache` Discover and cache the application's events and listeners<br>
`event:clear` Clear all cached events and listeners<br>
`event:generate` Generate the missing events and listeners based on registration<br>
`event:list` List the application's events and listeners<br>

**key**<br>
`key:generate` Set the application key<br>

**make**<br>
`make:cast` Create a new custom Eloquent cast class<br>
`make:channel` Create a new channel class<br>
`make:chart` Creates a new chart<br>
`make:command` Create a new Artisan command<br>
`make:component` Create a new view component class<br>
`make:controller` Create a new controller class<br>
`make:event` Create a new event class<br>
`make:exception` Create a new custom exception class<br>
`make:factory` Create a new model factory<br>
`make:job` Create a new job class<br>
`make:listener` Create a new event listener class<br>
`make:mail` Create a new email class<br>
`make:middleware` Create a new middleware class<br>
`make:migration` Create a new migration file<br>
`make:model` Create a new Eloquent model class<br>
`make:notification` Create a new notification class<br>
`make:observer` Create a new observer class<br>
`make:policy` Create a new policy class<br>
`make:provider` Create a new service provider class<br>
`make:request` Create a new form request class<br>
`make:resource` Create a new resource<br>
`make:rule` Create a new validation rule<br>
`make:scope` Create a new scope class<br>
`make:seeder` Create a new seeder class<br>
`make:test` Create a new test class<br>

**migrate**<br>
`migrate:fresh` Drop all tables and re-run all migrations<br>
`migrate:install` Create the migration repository<br>
`migrate:refresh` Reset and re-run all migrations<br>
`migrate:reset` Rollback all database migrations<br>
`migrate:rollback` Rollback the last database migration<br>
`migrate:status` Show the status of each migration<br>

**model**<br>
`model:prune` Prune models that are no longer needed<br>
`model:show` Show information about an Eloquent model<br>

**notifications**<br>
`notifications:table` Create a migration for the notifications table<br>

**optimize**<br>
`optimize:clear` Remove the cached bootstrap files<br>

**package**<br>
`package:discover` Rebuild the cached package manifest<br>

**publish**<br>
`publish:scheduled` Publish the scheduled command<br>

**queue**<br>
`queue:batches-table` Create a migration for the batches database table<br>
`queue:clear` Delete all of the jobs from the specified queue<br>
`queue:failed` List all of the failed queue jobs<br>
`queue:failed-table` Create a migration for the failed queue jobs database table<br>
`queue:flush` Flush all of the failed queue jobs<br>
`queue:forget` Delete a failed queue job<br>
`queue:listen` Listen to a given queue<br>
`queue:monitor` Monitor the size of the specified queues<br>
`queue:prune-batches` Prune stale entries from the batches database<br>
`queue:prune-failed` Prune stale entries from the failed jobs table<br>
`queue:restart` Restart queue worker daemons after their current job<br>
`queue:retry` Retry a failed queue job<br>
`queue:retry-batch` Retry the failed jobs for a batch<br>
`queue:table` Create a migration for the queue jobs database table<br>
`queue:work` Start processing jobs on the queue as a daemon<br>

**route**<br>
`route:cache` Create a route cache file for faster route registration<br>
`route:clear` Remove the route cache file<br>
`route:list` List all registered routes<br>

**sail**<br>
`sail:install` Install Laravel Sail's default Docker Compose file<br>
`sail:publish` Publish the Laravel Sail Docker files<br>

**sanctum**<br>
`sanctum:prune-expired` Prune tokens expired for more than specified number of hours.<br>

**schedule**<br>
`schedule:clear-cache` Delete the cached mutex files created by scheduler  <br>
`schedule:list` List the scheduled commands<br>
`schedule:run` Run the scheduled commands<br>
`schedule:test` Run a scheduled command<br>
`schedule:work` Start the schedule worker<br>

**schema**<br>
`schema:dump` Dump the given database schema<br>

**session**<br>
`session:table` Create a migration for the session database table<br>

**sitemap**<br>
`sitemap:generate` Generate the sitemaps<br>

**storage**<br>
`storage:link` Create the symbolic links configured for the application<br>

**stub**<br>
`stub:publish` Publish all stubs that are available for customization<br>

**vendor**<br>
`vendor:publish` Publish any publishable assets from vendor packages<br>

***view***<br>
`view:cache` Compile all of the application's Blade templates<br>
`view:clear` Clear all compiled view files

## Route<br>
### Define route
```
// Registering a get route with colsure: https://example.com/sheets
Route::get('sheets', function(){});

// Registering a get route with controller, logic is in index method of SheetCotroller.
Route::get('sheets', 'SheetController@index');
Route::get('sheets', [SheetController::class, 'index']);

// If a group of routes all utilize the same controller, you may use the controller method to define the common controller for all of the routes within the group.
Route::controller(SheetController::class)->group(function() {
    // Register routes here, following example refer to index method of the controller
    Route::get('sheets', 'index');
});
```

### HTTP Verbs
```
Route::options('sheets', function() {});
Route::get('sheets', function() {});
Route::post('sheets', function() {});
Route::put('sheets', function() {});
Route::patch('sheets', function() {});
Route::delete('sheets', function() {});
```

### RESTful Controllers
```
Every resource route create 7 routes
Route::resource('Sheets','SheetController');
```

```
// Specify a subset of actions to handle on the route
Route::resource('sheets', 'SheetController',['only' => ['index', 'show']]);
Route::resource('sheets', 'SheetController',['except' => ['edit', 'update', 'destroy']]);
```
### Route Prefixing
```
// We can pass an array of prefix, middleware, namespace and ... in group to apply to groups of routes
// Define a route group.
Route::group(['prefix' => 'admin'], function() {
    Route::get('sheets', function(){
        return 'Matches The "/admin/sheets" URL';
    });
});

// We can use array indexes out of group method
Route::prefix('admin-panel')->name('admin.')->namespace('Admin')->group(function() {
    //
});
```

### Route Parameters
```
// Registering a route that has a parameter
Route::get('sheets/{sheet}', function($sheet){});

// Registering a route that has an optional parameter
Route::get('users/{username?}', function($username = 'guest'){});
```
### Conditional route
```
// Registering a route that handle multiple verbs
Route::match(['get', 'post'], '/', function(){});

// Registering a route that handle all verbs
Route::any('sheets', function() {});

// Registering a route that match with specific pattern
Route::get('blog/{post}', function($post) {
    //
})->where('post', '[0-9]+');
Route::get('blog/{id}/{slug}', function($id, $slug) {
    //
})->where(['id' => '[0-9]+', 'slug' => '[A-Za-z]'])

// Set a pattern to be used across routes
Route::pattern('sheets', '[0-9]+')
```

### Sub-Domain Routing
```
// {my} will be passed to the closure
Route::group(['domain' => '{my}.example.com'], function(){});
```