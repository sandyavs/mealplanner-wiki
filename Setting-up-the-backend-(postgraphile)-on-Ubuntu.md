
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

Run the psql command, connecting as the postgres user, e.g:

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
$ psql -h 127.0.0.1
psql (12.4 (Ubuntu 12.4-0ubuntu0.20.04.1))
SSL connection (protocol: TLSv1.3, cipher: TLS_AES_256_GCM_SHA384, bits: 256, compression: off)
Type "help" for help.

username=# \q
```

Set up the mealplanner schema. Change to the `mealplanner/backend` directory and:

`psql -f db-reset.psql`

Next step: [[Setting up the GrapQL backend|Setting up the GraphQL backend]]
