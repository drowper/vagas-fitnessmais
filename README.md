## POC

Dashboard using php 8.4 with Laravel.

- Content:
    - [Stack](#stack)
    - [Installation](#installation)
    - [Running](#running)

## Stack <a name="stack"></a>

- Application Stack:
    - [PHP](https://www.php.net/)
    - [Laravel](https://laravel.com/)
    - [MySQL](https://www.mysql.com/)
    - [PHPUnit](https://phpunit.de/)

## Installation <a name="installation"></a>

Clone GIT repository.

```bash
# Using SSL method.
$ git clone git@github.com:drowper/vagas-fitnessmais.git
```

Access workdir of application:

```bash
$ cd vagas-fitnessmais/
```

Make a copy of .env.example for .env.

```bash
# Copy file.
$ cp .env.example .env
```

## Running <a name="running"></a>

Make sure you have [Docker](https://docs.docker.com/engine/install/) and [Docker Compose](https://docs.docker.com/compose/install/) installed.

Build the app image with the following command:

```bash
# Build app image.
$ docker compose build app
```

When the build is finished, you can run the environment in background mode with:

```bash
# Up and start all application containers.
$ docker compose up -d
```

We’ll now run composer install to install the application dependencies:

```bash
$ docker compose exec app rm -rf vendor
$ docker compose exec app composer install
```

The last thing we need to do is to generate a unique key with the artisan Laravel command-line tool. This key is used to encrypt user sessions and other sensitive data:

```bash
$ docker compose exec app php artisan key:generate
```
```bash
# Output
Application key set successfully.
```

Run all database migrations.

```bash
$ docker compose exec app php artisan migrate:refresh
```

Now go to your browser and access your server’s domain name or IP address on port 8000 (default: [localhost:8000/](http://localhost:8000/)):

```bash
$ http://server_domain_or_IP:8000
```

That's all folks!
```bash
=(^.^)=
```
