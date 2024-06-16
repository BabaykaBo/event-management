# Event Manager App
It is the pet project that is API for events management.

### Dependencies:

* PHP 8.1.10
* Laravel 10
* Composer 2.4.1
* Mailpit (test sending mails) 

For my project I used `MySql` 8.0 version.

### Installation:

1. Clone the project.

2. Install composer packages:
```commandline
composer install
```
3. Rename `.env.example` into `.env` (or make copy and rename it). Set database connection.

4. Use command for making migrations:
```commandline
php artisan migrate
```
5. Run server:
```commandline
php artisan serve
```
6. Sing up and enjoy!

6.1. If you want to create fast a bunch of users, events and attendees, you can use Seeder for it. Run terminal command:

```commandline
php artisan db:seed
```

Notice: all generated users has password `password`

## Features:

* Login and logout for users with tokens.
* CRUD for events.
* CRUD for attendees.
* Sending mails for reminding users about events.

See all routes: 
```commandline
php artisan route:list
```

Send mails command manually:
```commandline
php artisan app:send-event-reminder
```

Send mails automatically. It use Laravel schedule:
```commandline
php artisan schedule:work
```

Sending mails is queueable, so you also need to use this command:
```commandline
php artisan queue:work
```

I use <a href="https://mailpit.axllent.org/">Mailpit</a> for testing.
