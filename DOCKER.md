# Running with Docker (Laravel Sail)

## Start

```bash
./vendor/bin/sail up -d
```

App runs at `http://localhost`. Services: MySQL on port 3306, Redis on 6379.

## Stop

```bash
./vendor/bin/sail down
```

## Other useful commands

```bash
# View logs
./vendor/bin/sail logs

# Run artisan commands
./vendor/bin/sail artisan migrate

# Open a shell inside the container
./vendor/bin/sail shell

# Rebuild containers (after changing compose.yaml)
./vendor/bin/sail build --no-cache
```

## Optional alias

Add to your `~/.zshrc` or `~/.bashrc` to type `sail` instead of `./vendor/bin/sail`:

```bash
alias sail='./vendor/bin/sail'
```

## First-time setup

Copy the example env file before starting:

```bash
cp .env.example .env
```