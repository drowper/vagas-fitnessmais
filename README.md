## FITNESSMAIS VAGAS

Dashboard para seleção de candidatos, cadastro de vagas e download de currículos.

- Content:
    - [Stack](#stack)
    - [Installation](#installation)
    - [Running](#running)
    - [Tests](#tests)

## Stack <a name="stack"></a>

- Stack:
    - [php](https://www.php.net/)
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

For create and run containers.

```bash
# Up and start all application containers.
$ docker compose up -d
```

Enter into app container:

```bash
$ docker exec -it app bash
```

Install php dependencies with [Composer](https://getcomposer.org/)

```bash
$ compose install
```

Run all database migrations.

```bash
$ php artisan migrate
```

## Test <a name="tests"></a>

For run app:

```bash
# Running unit tests.
$ http://localhost:8080
```
