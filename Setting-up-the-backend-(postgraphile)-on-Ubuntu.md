
`sudo apt install postgresql`

This will set up a default postgres instance in the default location(s)

On Ubuntu, Postgres listens only on localhost by default. There's no need to reconfigure the server or add firewall rules. 

Next, setup trusted sign on for your Ubuntu user account in postgres. This will allow password-less access to postgres based on your logged-in user.  Edit the file pg_hba.conf in the postgres main instance config directory (e.g `sudo nano /etc/postgresql/12/main/pg_hba.conf`).

At the bottom of the file look for the

`# IPv4 local connections:`

There should be one line under it that looks like:

`host    all             all             127.0.0.1/32            md5`

make a copy of this line, above it and edit it so that the IPv4 section looks like:

```
# IPv4 local connections:
host    sameuser             all             127.0.0.1/32            trust
host    all             all             127.0.0.1/32            md5
```
With that one line added, save and close the file and restart postgres:

`sudo systemctl restart postgresql`

Open a command prompt and run the psql command, connecting as the postgres user, e.g:

`sudo -u postgres psql`

run the following two sql commands, substituting your Ubuntu login username in place of UserName (it is case sensitive):

```
CREATE ROLE "UserName" WITH LOGIN  SUPERUSER  INHERIT  CREATEDB  CREATEROLE  NOREPLICATION;
CREATE DATABASE "UserName";
```

then quit psql with:
`\q`

To test that all the above worked, you should be able to use psql to connect to your database on localhost without needing to provide a username or password:

```
psql -h 127.0.0.1
psql (13.0)
Type "help" for help.

UserName=#
```

Set up the mealplanner schema. Change to the `mealplanner/backend` directory and:

`psql -f db-reset.psql`

Next step: [[Setting up the GrapQL backend|Setting up the GraphQL backend]]
