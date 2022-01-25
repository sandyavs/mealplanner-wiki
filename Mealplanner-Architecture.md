# Application Tiers

Mealplanner is essentially a 3-tier application with a UI (or front end) that executes entirely in the client's browser, a middleware server that presents a single graphql API and postgres database backend. The front end is a React app based on React Hooks and React Material UI components. The middleware is Postgraphile which is a NodeJS service that automatically generates a graphql API and schema from the structure of a relational database. Finally the application's database schema is hosted in postgres. More on each of these component tiers below.

## React Front End

TBC

## Postgraphile

Postgraphile provides a complete graphql API mapped to a postgres database schema. It is a virtually zero code implementation where all nodes and edges are built from the relational schema. As such the database defines the API in a declarative manner, and various postgres DDL features allow for tuning the API. From the [Postgraphile site](https://www.graphile.org/postgraphile/):

```
PostGraphile automatically detects tables, columns, indexes, relationships, views, types, functions, comments, and more — providing a GraphQL server that is highly intelligent about your data, and that automatically updates itself without restarting when you modify your database.
```

This is an ideal choice for this project for a number of reasons:
* Developers can focus on front end and database, eliminating the need for middleware developers
* The common denominator knowledge base for data modelling among many devs is relational data and ERDs
* SQL skills are more common than API design skills
* All data definition, managment and access control is centralised in the DB and defined with SQL
* Since the data model and schema are fairly stable, the API is also very stable

[[mealplanner-graphl-schema.png]]

## Postgres

In a sense this choice was made moot by the selection of Postgraphile which only works with Postgres. However, postgres is an excellent choice for an RDBMS; it is an enterprise class DB service with an incredible range of features, capabilities and scaling. Postgres' `plpgsql` programming language is rich enough to allow encoding all rules for data management and access right into the database.

### Database Schema

Mealplanner actually uses two schema, `app` and `pp_private`. The first is the main schema from which the GraphQL API is built and it defines all the tables, relationships and functions that support the API. The private schema hoolds account information to support authentication.

[[mealplanner-db.png]]

 
