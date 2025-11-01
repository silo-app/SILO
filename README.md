WARNING: THIS PACKAGE IS CURRENTLY UNDER DEVELOPMENT

<p align="center">
    <img width="300" alt="SILO logo" src="https://raw.githubusercontent.com/silo-app/assets/refs/heads/main/images/SILO_logo_full.png">
</p>

SILO is a warehouse software for monitoring parts and stocks of all kinds.

## Setup development instance

### Prepare environment
```bash
$ mkdir silo && cd silo
$ git clone https://github.com/silo-app/silo-api.git
$ git clone https://github.com/silo-app/SILO.git
$ cd SILO
$ cp .env.example .env.development
```

### Start container using `docker-compose.dev.yml`
```bash
$ docker-compose -f docker-compose.yml -f docker-compose.dev.yml up --build
```
