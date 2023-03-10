# Docker environment with PHP 8.0, MySQL 8.0, Nginx and some other services

## Requirements

- Docker
- Docker compose v1 or v2

## Running the project with Docker Compose

### After cloning the repository from gitHub:

Copy .env.example (if `.env` file not exists):

```bash
cp .env.example .env
```

and set some parameters in `.env` file,
for example, `FORWARD_DB_PORT`, `FORWARD_REDIS_PORT`, `DB_PASSWORD`, `DB_HOST` etc,
if needed!

Then run:

```bash
docker compose build 
docker compose up -d
```

### Running unit tests:

```bash
docker compose exec app ./vendor/bin/phpunit tests
```
