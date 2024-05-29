### Setup Postgress in Docker

<p align="center">
  <img src="https://djeqr6to3dedg.cloudfront.net/repo-logos/library/docker/live/logo.png" />
  <img src="https://djeqr6to3dedg.cloudfront.net/repo-logos/library/postgres/live/logo.png" />
</p>

---

- Run the `docker-compose.yml`

```bash
docker-compose up -d
```

---

- Install `xampp`
- Active these two extension in `php.ini` file under `xampp`

```
extension=pgsql
extension=pdo_pgsql
```

- Download `adminer` - https://www.adminer.org
- Move the `Adminer php` file into `xampp htdocs` folder
- Run `xampp control panel` and start the `Appache server` and click - `Admin` button

---

#### Some useful docker commands

- Docker Container List

```bash
docker ps
```

- Docker Container Logs

```bash
docker log <CONTAINER_ID>
```

- Live data stream for running containers

```bash
docker stats
```

---

How to import `sql` file using `docker` command:

- Open the cmd.
- Execute the `docker ps` command to get the container ID.
- User `docker cp D:\2024-05-29.sql <container_id>:/2024-05-29.sql` command to copy the .sql file from local storage to docker container.
- Start a bash session within the container by running: `docker exec -it <container_id> bash` command.
- Import the .sql file into the PostgreSQL database: `psql -U <user> -d <database_name> -f /2024-05-29.sql`

---
