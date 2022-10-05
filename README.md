
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

Create new laravel project using composer\  
`composer create-project laravel/laravel folder_name`

Composer install will install the dependencies into the vendor directory as specified in the composer.lock file.\  
`composer install`

will update your dependencies as they are specified in `composer.json`\  
`composer update`

It just regenerates the list of all classes that need to be included in the project.\  
`composer dump-autoload [--optimize]`

It will update composer.\  
`composer self-update`

Add new package to the project.\  
`composer require [options] [--] [vender/packages]...`

Install laravel installer globally.\  
`composer global require laravel/installer`

Install laravel using laravel installer.\  
`Laravel new project`

Create .env from .env.example.\  
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

**auth**
`auth:clear-resets` Flush expired password reset tokens
**cache**
`cache:clear` Flush the application cache
`cache:forget` Remove an item from the cache
`cache:table` Create a migration for the cache database table
**config**
`config:cache` Create a cache file for faster configuration loading
`config:clear` Remove the configuration cache file
**db**
`db:monitor` Monitor the number of connections on the specified database
`db:seed` Seed the database with records
`db:show` Display information about the given database
`db:table` Display information about the given database table
`db:wipe` Drop all tables, views, and types
**env**
`env:decrypt` Decrypt an environment file
`env:encrypt` Encrypt an environment file
**event**
`event:cache` Discover and cache the application's events and listeners
`event:clear` Clear all cached events and listeners
`event:generate` Generate the missing events and listeners based on registration
`event:list` List the application's events and listeners
**key**
`key:generate` Set the application key
**make**
`make:cast` Create a new custom Eloquent cast class
`make:channel` Create a new channel class
`make:chart` Creates a new chart
`make:command` Create a new Artisan command
`make:component` Create a new view component class
`make:controller` Create a new controller class
`make:event` Create a new event class
`make:exception` Create a new custom exception class
`make:factory` Create a new model factory
`make:job` Create a new job class
`make:listener` Create a new event listener class
`make:mail` Create a new email class
`make:middleware` Create a new middleware class
`make:migration` Create a new migration file
`make:model` Create a new Eloquent model class
`make:notification` Create a new notification class
`make:observer` Create a new observer class
`make:policy` Create a new policy class
`make:provider` Create a new service provider class
`make:request` Create a new form request class
`make:resource` Create a new resource
`make:rule` Create a new validation rule
`make:scope` Create a new scope class
`make:seeder` Create a new seeder class
`make:test` Create a new test class
**migrate**
`migrate:fresh` Drop all tables and re-run all migrations
`migrate:install` Create the migration repository
`migrate:refresh` Reset and re-run all migrations
`migrate:reset` Rollback all database migrations
`migrate:rollback` Rollback the last database migration
`migrate:status` Show the status of each migration
**model**
`model:prune` Prune models that are no longer needed
`model:show` Show information about an Eloquent model
**notifications**
`notifications:table` Create a migration for the notifications table
**optimize**
`optimize:clear` Remove the cached bootstrap files
**package**
`package:discover` Rebuild the cached package manifest
**publish**
`publish:scheduled`      Publish the scheduled command  
**queue**
`queue:batches-table` Create a migration for the batches database table
`queue:clear` Delete all of the jobs from the specified queue
`queue:failed` List all of the failed queue jobs
`queue:failed-table` Create a migration for the failed queue jobs database table
`queue:flush` Flush all of the failed queue jobs
`queue:forget` Delete a failed queue job
`queue:listen` Listen to a given queue
`queue:monitor` Monitor the size of the specified queues
`queue:prune-batches` Prune stale entries from the batches database
`queue:prune-failed` Prune stale entries from the failed jobs table
`queue:restart` Restart queue worker daemons after their current job
`queue:retry` Retry a failed queue job
`queue:retry-batch` Retry the failed jobs for a batch
`queue:table` Create a migration for the queue jobs database table
`queue:work` Start processing jobs on the queue as a daemon
**route**
`route:cache` Create a route cache file for faster route registration
`route:clear` Remove the route cache file
`route:list` List all registered routes
**sail**
`sail:install` Install Laravel Sail's default Docker Compose file
`sail:publish` Publish the Laravel Sail Docker files
**sanctum**
`sanctum:prune-expired` Prune tokens expired for more than specified number of hours.
**schedule**
`schedule:clear-cache` Delete the cached mutex files created by scheduler  
`schedule:list` List the scheduled commands
`schedule:run` Run the scheduled commands
`schedule:test` Run a scheduled command
`schedule:work` Start the schedule worker
**schema**
`schema:dump` Dump the given database schema
**session**
`session:table` Create a migration for the session database table
**sitemap**
`sitemap:generate` Generate the sitemaps
**storage**
storage:link           Create the symbolic links configured for the application
**stub**
`stub:publish` Publish all stubs that are available for customization
**vendor**
`vendor:publish` Publish any publishable assets from vendor packages
***view***
`view:cache` Compile all of the application's Blade templates
`view:clear` Clear all compiled view files