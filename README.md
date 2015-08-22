# Database Tasks
This repo gives help for various database import and export features, for now it includes:
* mysql,
* postgresql and 
* mongodb

### Postgresql
* Take Backup

```sh
$ pg_dump -W -U {username} {source_db_name} -f backup.sql -h localhost
```

* Restore Backup

```sh
$  psql -U {username} -d {destination_db_name} -f backup.sql -h localhost
```

* Backup a specific table

```sh
$ pg_dump --table {table_name} -U {username} {source_dbname} -f table.sql -h localhost
```

* Restore a specific table

```sh
$ psql -f table.sql {destination_dbname} -U {username} -h localhost
```

* Backup and restore on remote server

```sh
$ pg_dump dbname | psql -h hostname dbname
```
