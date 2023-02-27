# Docker Postgres Server
A simple docker setup to run a Postgres server accessible via localhost. Based off the following example:
https://github.com/khezen/compose-postgres/blob/master/docker-compose.yml


if using this in a new project, be sure to update the following configuration settings in the docker-compose.yml file:
- container_name
- volumes
- Postgres_DATABASE

### start docker
```sh
docker-compose up -d
```

### stop docker
```sh
docker-compose down
```

### stop docker and delete volumes (databases)
```sh
docker-compose down -v
```

### log into the container
```sh
docker exec -it docker_postgres_server /bin/bash
```

### export the database (run outside of postgres shell)
```sh

```

### import a database (run outside of postgres shell)
```sh

```

### log into the postgres shell
```sh

```

## Postgres connection settings
These setttings can be used in your project settings or database management application (sequel pro)
| KEY | VALUE |
| ------ | ------ |
| HOST | 127.0.0.1 |
| USER | postgres |
| DATABASE | docker_postgres_database |
| PASSWORD | dbpw |
| PORT | 5432 |

## Viewing the database using pgAdmin

### Access to PgAdmin in the browser: 
| KEY | VALUE |
| ------ | ------ |
| URL | http://localhost:5050 |
| PASSWORD | admin (as a default) |


### Add a new server in PgAdmin:
| KEY | VALUE |
| ------ | ------ |
| HOST | postgres |
| USER | postgres |
| PASSWORD | dbpw |
| PORT | 5432 |