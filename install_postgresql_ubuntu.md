# Install Postgresql Ubuntu
Source: [https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04)
[http://stackoverflow.com/questions/28253681/you-need-to-install-postgresql-server-dev-x-y-for-building-a-server-side-extensi](http://stackoverflow.com/questions/28253681/you-need-to-install-postgresql-server-dev-x-y-for-building-a-server-side-extensi)

### Install
```
sudo apt-get update
sudo apt-get install postgresql postgresql-contrib
```

### Switching Over to the postgres Account
The installation procedure created a user account called postgres that is associated with the default Postgres role. 
In order to use Postgres, we can log into that account.

```
sudo -i -u postgres
```
Access a Postgres prompt by typing:

```
psql
```

Exit out of the PostgreSQL prompt by typing:

```
\q
```

### Create a New Role
If you are logged in as the postgres account, you can create a new user by typing:

```
createuser --interactive
```

```
Enter name of role to add: zet
Shall the new role be a superuser? (y/n) y
```
### Create a New Database
Create database with the same name as the role being used to login

```
createdb zet
```

### Logout postgres user

```
exit
```
### Open a Postgres Prompt with the New Role

```
sudo -i -u zet
psql
```

### Install psycopg2 for Python
```
sudo apt-get install python-psycopg2
sudo apt-get install libpq-dev
```


