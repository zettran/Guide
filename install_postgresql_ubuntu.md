# Install Postgresql Ubuntu

### Install
sudo apt-get update
sudo apt-get install postgresql postgresql-contrib

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
The script will prompt you with some choices and, based on your responses, execute the correct Postgres commands to create a user to your specifications.

```
Enter name of role to add: zet
Shall the new role be a superuser? (y/n) y
```
### Create a New Database
Create database with the same name as the role being used to login

```
createdb zet
```


