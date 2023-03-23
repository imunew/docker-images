# typos-cli
This is a `Dockerized` [crate-ci/typos](https://github.com/crate-ci/typos).

## How to use (with Docker)

```bash
$ docker run --rm -t -v "/path/to/app:/app" imunew/typos-cli /app --format json
```

## How to use (with Docker Compose)

```yaml
# docker-compose.yml
typos-cli:
  image: imunew/typos-cli
  volumes:
    - /path/to/app:/app:cached
```

```bash
$ docker compose run --rm typos-cli /app --format json
```
