# PostgreSQL

## Installation

Install PostgreSQL on your system, with either the docker container or a bare metal installation.

## Admin authentication method

In the file `pg_hba.conf`, usually found in `/etc/postgresql/9.1/main/pg_hba.conf`, change

```
local   all             postgres                                peer
```

to

```
local   all             all                                md5
```

### Restart PostgreSQL

```
sudo service postgresql restart
```

## Database dumps

SQL-Tasks require a populated database.

### Create the `task_db`.

```
CREATE DATABASE task_db;
```

### Create user

```
CREATE USER my_username WITH PASSWORD 'my_password';
```

### Grant privileges

```
GRANT ALL PRIVILEGES ON DATABASE "task_db" to my_username;
```

The SemanticSQL-Task requires the manipulated imdb-database.
The SQL-Task requires the northwind-database.

The dumps can be downloaded from the following links:

### Northwind

- [attibutes](https://aladin.htw-dresden.de/file/db_files/northwind/northwind.tsv)

### IMDB

- [attibutes](https://aladin.htw-dresden.de/file/db_files/imdb/attributes.tsv)
- [names](https://aladin.htw-dresden.de/file/db_files/imdb/names.tsv)
- [professions](https://aladin.htw-dresden.de/file/db_files/imdb/professions.tsv)
- [title](https://aladin.htw-dresden.de/file/db_files/imdb/title.tsv)
- [characters](https://aladin.htw-dresden.de/file/db_files/imdb/characters.tsv)
- [person_profession](https://aladin.htw-dresden.de/file/db_files/imdb/person_profession.tsv)
- [regions](https://aladin.htw-dresden.de/file/db_files/imdb/regions.tsv)
- [title\_\_](https://aladin.htw-dresden.de/file/db_files/imdb/title__.tsv)
- [formats](https://aladin.htw-dresden.de/file/db_files/imdb/formats.tsv)
- [languages](https://aladin.htw-dresden.de/file/db_files/imdb/languages.tsv)
- [person_title](https://aladin.htw-dresden.de/file/db_files/imdb/person_title.tsv)
- [title_genre](https://aladin.htw-dresden.de/file/db_files/imdb/title_genre.tsv)
- [types](https://aladin.htw-dresden.de/file/db_files/imdb/types.tsv)
- [genres](https://aladin.htw-dresden.de/file/db_files/imdb/genres.tsv)
- [localization](https://aladin.htw-dresden.de/file/db_files/imdb/localization.tsv)
- [person](https://aladin.htw-dresden.de/file/db_files/imdb/person.tsv)
- [title_names](https://aladin.htw-dresden.de/file/db_files/imdb/title_names.tsv)
- [years](https://aladin.htw-dresden.de/file/db_files/imdb/years.tsv)

### To restore a dump execute

```
psql -U my_username -d task_db

set search_path to "imdb2";
\i imdb.sql

set search_path to "northwind";
\i northwind.sql
```
