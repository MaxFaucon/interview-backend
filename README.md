# Welcome

Bellow you'll find the instructions you must complete to successfully pass the test.

May the force be with you.

# How to

* Fork the repository and make your changes in your own private fork
* Invite c.noterdaem@soilcapital.com to the fork

## What needs to be done

- Be a hacker: find a way to successfully run the app and get the right JSON output from the API endpoint /v1/auth/ - hint: no code change needed (but think of Composer + check Laravel doc https://laravel.com/docs/9.x).
- Be a saviour: fix a bug in the app. /v1/auth/debug?lang=fr should return a JSON with a `language` key containing the string "Français".
- Be a builder: add a new API endpoint to the app and fetch some external API data as JSON. Example, from: https://official-joke-api.appspot.com/random_joke.

## Exercise solutions

- Be a hacker: 
    1. Remove `classmap` section from `composer.json` file since the folder `app/Classes` doesn't exist.
    2. Use `composer install` to install all the required packages.
    3. Add an empty `storage/framework/cache/data` directory, otherwise there is an error when using `php artisan serve`.
    4. Start the application using the `php artisan serve` command.
- Be a saviour: In the `debug()` function of the `AuthController` file, replace `$params["language"]` by `$params["lang"]` since the query parameter name used in the URL is called `lang`.
