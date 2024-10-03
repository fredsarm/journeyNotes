# 1. Introduction to PostgreSQL

## Technical requirements

### PostgreSQL at a glance
- A brief history of PostgreSQL
- What’s new in PostgreSQL 16?
- PostgreSQL release policy, version numbers, and life cycle
- Exploring PostgreSQL terminology
### Installing PostgreSQL
- What to install
#### Installing PostgreSQL from binary packages
- Using the book’s Docker images
- Installing PostgreSQL on GNU/Linux Debian, Ubuntu, and derivatives
- Installing PostgreSQL on Fedora Linux
- Installing PostgreSQL on FreeBSD
#### Installing PostgreSQL from sources

#### Installing PostgreSQL via pgenv

# 2. The cluster
## 2.1. Connecting to the cluster
When you initialize the cluster with the **initdb** command, PostgreSQL builds the filesystem layout of the PGDATA directory and builds two template databases named template0 and template1, to be used as a starting point to clone other new databases. 
You need a client to connect with one of the databases. PostgreSQL ships with a client named psql. Other applications need a so-called connection string, a URI indicating all the required parameters to connect to the database. 
### 2.1.1. The Template Databases
The first database created is `template1` that is cloned into `template0`. Both are identical, and the aim of `template0` is to act as a safe copy of the `template1`. Whatever object you put into `template1`, you will find the very same object in freshly created databases.  
You cannot connect to `template0` in order to prevent accidental damage 
These templates are not fundamental for the other databases to run, they're just a safe copy.
There’s a third database that is created during the installation process: the `postgres` database, that belongs to the `postgres` user. This is be used for connections instead of the template databases.
### 2.1.2. The psql command-line client