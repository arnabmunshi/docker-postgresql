### Setup Postgress in Docker

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
