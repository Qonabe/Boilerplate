# Laravel

## Prerequisite

Environment Setup: Github

[Composer](https://getcomposer.org/)
[Node and NPM](https://nodejs.org/en)

TODO:Add PATH edit

## Installation

### Create the project

`composer create-project laravel/laravel example-app`

ou bien

```
composer global require laravel/installer

laravel new example-app
```

### Create the database

[Edit the database section of .env](https://laravel.com/docs/10.x/configuration#environment-configuration).

`php artisan migrate`

## Run

`php artisan serve`

## Addons

### Setting up XDebug

- Check if the PHP you're using has the XDebug module with the [XDebug Installation Wizard](https://xdebug.org/wizard). If not, just follow the instructions
- Get the XDebug port from phpinfo()
- Check the debugger is listening to the correct port

### Adding PHP Prettier to the project

- `npm install prettier@2.8.8 @prettier/plugin-php`
- (Restart code editor)
