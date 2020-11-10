# Postgres on Windows

https://www.postgresql.org/download/windows/

The installer is a bit of a pig, but once installed it won't have much impact on your system.

Go with defaults, pick a *good* password and remember it or put it in a password manager.

Don't bother running the StackBuilder wizard at the end, none of the extras are needed.

On windows, Postgres listens on all interfaces by default. This isn't particularly secure for a dev workstation so configure it to listen to localhost only.

In the installation directory find `data\postgresql.conf` (e.g. `C:\Program Files\PostgreSQL\13\data\postgresql.conf`).

Edit it and change

`listen_addresses = '*'`

to 

`listen_addresses = 'localhost'`

Save and close 

Next, setup trusted sign on for your windows user account in postgres. This will allow password-less access to postgres based on your logged-in user.  Edit the file pg_hba.conf in your postgres data directory (e.g `"\Program Files\PostgreSQL\13\data\pg_hba.conf"`).

At the bottom of the file look for the

`# IPv4 local connections:`

There should be one line under it that looks like:

`host    all             all             127.0.0.1/32            scram-sha-256`

make a copy of this line, above it and edit it so that the IPv4 section looks like:

`# IPv4 local connections:

host    UserName             UserName             127.0.0.1/32            trust

host    all             all             127.0.0.1/32            scram-sha-256`

Where "`UserName`" is your user name as it appears when you open a Windows command prompt. It is case sensitive.

Repeat for the IPv6 section next so that it looks like:

`# IPv6 local connections:

host    UserName             UserName             ::1/128                 trust

host    all             all             ::1/128                 scram-sha-256`

With those two lines added, save and close the file.

then restart postgresql in the Windows services management panel.

Open a command prompt and run the psql command, connecting as the postgres user, e.g:

`"\Program Files\PostgreSQL\13\bin\psql.exe" -U postgres`

provide the password you used when installing postgres.

run the following two sql commands:

`CREATE ROLE "UserName" WITH  LOGIN  SUPERUSER  INHERIT  CREATEDB  CREATEROLE  NOREPLICATION;

CREATE DATABASE "UserName";`

then quit psql with:
`\q`

Once again, "UserName" must match your Windows username as it appears on the command prompt and it is case sensitive.

To test that all the above worked, you should be able to use psql to connect to your database on localhost without needing to provide a username or password:

`"\Program Files\PostgreSQL\13\bin\psql.exe" -h 127.0.0.1

psql (13.0)

Type "help" for help.


UserName=#`

You may get a warning about the windows codepage. ignore it. Quit again with `\q`

Set up the mealplanner schema:

`"\Program Files\PostgreSQL\13\bin\psql.exe" -f db-reset.psql`

Install node using the windows installer from nodejs.org

Open a command prompt or powershell and CD to the `mealplanner/backend`

Install the dependencies if you haven't already:

`npm install`

Now run the graphql server:

`npm start`

The server should now be available at `http://localhost:4000/graphiql`

