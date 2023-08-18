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

## Docker Content Trust (DCT)
The docker image is signed by `docker trust sign`.

```bash
$ docker trust inspect --pretty imunew/typos-cli:1.16.5

Signatures for imunew/typos-cli:1.16.5

SIGNED TAG   DIGEST                                                             SIGNERS
1.16.5       42c390913ce53f78912d970a9491d5cbfcad874d0092fd8aa4ac282ecba2b3cd   docker-imunew

List of signers and their keys for imunew/typos-cli:1.16.5

SIGNER          KEYS
docker-imunew   3f7c0d04e81b

Administrative keys for imunew/typos-cli:1.16.5

  Repository Key:       26fc09e595d96fb11a696b97897c96f3a0c9c983680bf09bc55eea010f89bb5a
  Root Key:     2699423afb07f3ae20e1b314d4552d0538be366ff5ed82922e7c83ad776aa37a
```
