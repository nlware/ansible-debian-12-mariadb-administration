## debian-12-mariadb-administration

[![CI](https://github.com/nlware/ansible-debian-12-mariadb-administration/workflows/CI/badge.svg)](https://github.com/nlware/ansible-debian-12-mariadb-administration/actions?query=workflow%3ACI)

Administer databases and users on MariaDB server in Debian 12.

#### Variables

* `debian_12_mariadb_administration_databases_present`: [default: `{}`]: Databases to create
* `debian_12_mariadb_administration_databases_present.{n}.name`: [required]: The name of the database
* `debian_12_mariadb_administration_databases_present.{n}.collation`: [optional, default: `utf8mb4_general_ci`]: The collation of the database
* `debian_12_mariadb_administration_databases_present.{n}.encoding`: [optional, default: `utf8mb4`]: The character set of the database

* `debian_12_mariadb_administration_databases_absent`: [default: `[]`]: Databases to drop

* `debian_12_mariadb_administration_users_present`: [default: `[]`]: Users to create
* `debian_12_mariadb_administration_users_present.{n}.name`: [required]: The name of the user
* `debian_12_mariadb_administration_users_present.{n}.password`: [required]: The password of the user
* `debian_12_mariadb_administration_users_present.{n}.priv`: [optional, default: `name + '.*:ALL'`]: Privileges
* `debian_12_mariadb_administration_users_present.{n}.host`: [optional, default: `localhost`]: Host to create privileges for

* `debian_12_mariadb_administration_users_absent`: [default: `[]`]: Users to drop
* `debian_12_mariadb_administration_users_absent.{n}.name`: [required]: The name of the user
* `debian_12_mariadb_administration_users_absent.{n}.host`: [optional, default: `localhost`]: Host to drop privileges for
