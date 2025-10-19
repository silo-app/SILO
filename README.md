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
```

#### Create `.env.development`

```environment
POSTGRES_HOST=postgres
POSTGRES_PORT=5432
POSTGRES_DB=silo_db
POSTGRES_USER=silo
POSTGRES_PASSWORD=devpostgresqlpassword

SILO_POSTGRES_DATABASE_URI=postgresql+asyncpg://${POSTGRES_USER}:${POSTGRES_PASSWORD}@${POSTGRES_HOST}:${POSTGRES_PORT}/${POSTGRES_DB}
SILO_JWT_SECRET_KEY=silojwtsecretkey123
SILO_FIRST_ADMIN_USER=csmith
SILO_LDAP_ALLOWED_GROUPS=["cn=Admins,ou=groups,dc=mokapi,dc=io"]
SILO_LDAP_BASE_DN=dc=mokapi,dc=io
SILO_LDAP_USER_DN_TEMPLATE=uid={username},dc=mokapi,dc=io
SILO_LDAP_SSL_SKIP_VERIFY=1
```

### Start container using `docker-compoer.dev.yml`
```bash
$ docker-compose -f docker-compose.yml -f docker-compose.dev.yml up --build
```