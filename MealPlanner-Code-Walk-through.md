## Frontend

We are using HTML, CSS, JavaScript with React, Relay, Material-UI on Front end. 

Webpack is a bundler that takes CSS, JS, JSX, HTML, images, fonts and converts it into static assets of normal HTML, CSS, JS. Webpack Dev Server (default for React Scripts) is a bundler as development server for serving the front end application. We need Webpack Dev Server so that it renders as and when a file is changed. It is known as HMR (Hot Module Reloading). We access the Webpack Dev Server via localhost:3000.

Webpack use Babel as the transpiler in the development side for transpiling. Transpiling is when you have the source and the target in the same language and basically transpile from one version to another version. We moved to TypeScript. Babel can compile TypeScript to JavaScript.

## API

We use the library Postgraphile for the API. Postgraphile basically implements the API protocol GraphQL. Usually the RestAPIs are implemented with http router library like express, that uses the post, get, put, delete HTTP methods. Whereas GraphQL has only one endpoint /graphql with post method.

We access the Postgraphile via the Graph interactive query language (Graphiql)

http://localhost:4000/graphiql 

To start this server, we use `docker-compose up` (Docker compose is an orchestration tool that brings up all containers such as postgraphile, postgres, webpack dev server).

Write an operation type mutation with operation name login calling the mutation authenticate. 

Before April 2022, the jwtToken was generated and it needed to be assigned to a Bearer token like described below:

```jsx
mutation login {
  authenticate(
    input: {
      userEmail: "mealdesigner@example.com"
      password: "681d62a975c7cc6"
    }
  ) {
    jwtToken
  }
}
```

When the mutation is run, it returns the jwtToken.

Copy the token within quotes eg: 

```jsx
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJyb2xlIjoiYXBwX21lYWxfZGVzaWduZXIiLCJwZXJzb25faWQiOiIyIiwiZXhwIjoxNjM4ODA3MjE2LCJpYXQiOjE2MzgyMDI0MTUsImF1ZCI6InBvc3RncmFwaGlsZSIsImlzcyI6InBvc3RncmFwaGlsZSJ9.3_J_B8QJzZ0cuJkPdbh9BMlEnlwpDiMQS00kvTAlu2U
```

Inside Request Headers, create a JSON object as below:

```jsx
{"Authorization":"Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJyb2xlIjoiYXBwX21lYWxfZGVzaWduZXIiLCJwZXJzb25faWQiOiIyIiwiZXhwIjoxNjM4ODA3MjE2LCJpYXQiOjE2MzgyMDI0MTUsImF1ZCI6InBvc3RncmFwaGlsZSIsImlzcyI6InBvc3RncmFwaGlsZSJ9.3_J_B8QJzZ0cuJkPdbh9BMlEnlwpDiMQS00kvTAlu2U"}
```

Note: This jwtToken can be decoded in [[jwt.io](http://jwt.io/)](http://jwt.io) eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJyb2xlIjoiYXBwX21lYWxfZGVzaWduZXIiLCJwZXJzb25faWQiOiIyIiwiZXhwIjoxNjQzNzQ4MzQ4LCJpYXQiOjE2NDMxNDM1NDcsImF1ZCI6InBvc3RncmFwaGlsZSIsImlzcyI6InBvc3RncmFwaGlsZSJ9.klY0l0vs3q6c-pF8n-O_xs4o2H5ro9kgapsICIiROJw

decodes to a payload of 

{
"role": "app_meal_designer",
"person_id": "2",
"exp": 1643748348,
"iat": 1643143547,
"aud": "postgraphile",
"iss": "postgraphile"
}

On April 2022, we updated the code to support express session based authentication. This moves away from Bearer token based auth scheme to a simpler httponly cookie based auth scheme. This is much simpler to implement on the client side and also make it more secure. For this we need to write an operation type mutation with operation name login calling the mutation authenticate as follows:

```jsx
mutation login {
  authenticate(
    input: {
      userEmail: "mealdesigner@example.com"
      password: "681d62a975c7cc6"
    }
  ) {
    jwtToken {
			exp
			role
			personId
		}
  }
}
```

This gives the following output and also sets a cookie identifying the user.

```jsx
{
	"data": {
		"authenticate": {
			"jwtToken": {
				"exp": "1706106884",
				"role": "app_admin",
				"personId": "1"
			}
		}
	}
}

```

This set cookie can be also viewed in the Network tab of Developer tools.


<img width="720" alt="Network" src="https://github.com/CivicTechFredericton/mealplanner/assets/57197486/5ca78616-1c6d-4794-9239-566896ef40f2">

If we copy the session content eyJwZXJzb25faWQiOiIxIiwicm9sZSI6ImFwcF9hZG1pbiJ9 and do a base64 decoding we will get the person id and the role

```graphql
❯ pbpaste | base64 -d
{"person_id":"1","role":"app_admin"}%
```

To verify whether authorization is successful create and run the query as below

```jsx
query currentUser {
  currentPerson {
    fullName
		email
  }
}
```

This would give the output as 

```jsx
{
	"data": {
		"currentPerson": {
			"fullName": "Admin",
			"email": "admin@example.com"
		}
	}
}
```

To understand how postgraphile sends the query or mutation as a single SELECT statement to postgres and gets it as a JSON object, let's consider this example:

```graphql
query simplePlans {
  mealPlans {
    nodes {
      id
      nameEn
      person {
        fullName
      }
    }
  }
}
```

This graphql query basically translates to a SQL query. It is explained below. If you notice the output it has an 'explain' section which shows

```jsx
with __local_0__ as (select to_json((**json_build_object**('__identifiers'::text, **json_build_array**(((__local_1__."id")::numeric)::text), '**nameEn**'::text, (__local_1__."**name_en**"), '**@person**'::text, (select **json_build_object**('__identifiers'::text, json_build_array(((__local_2__."id")::numeric)::text), '**fullName**'::text, (__local_2__."**full_name**")) as object
from "**app"."person**" as __local_2__

where (__local_1__."person_id" = __local_2__."id") and (TRUE) and (TRUE)

)))) as "**@nodes**" from (select __local_1__.*
from "**app"."meal_plan**" as __local_1__

where (TRUE) and (TRUE)
order by __local_1__."id" ASC

) __local_1__), __local_3__ as (select json_agg(to_json(__local_0__)) as data from __local_0__) select coalesce((select __local_3__.data from __local_3__), '[]'::json) as "data";
```

The above query builds a json object as an array with the fields requested such as nameEn and fullName. This is query selected from the table app.person with the snake case column names name_en and full_name for the table app.meal_plan for a particular person_id which shows it in as ascending order. json_agg makes all the rows returned into an array.

If we run this in psql prompt 

```jsx
docker-compose exec db psql -U postgres

```

it gives you the response

```jsx
data
-------------------------------------------------------------------------------------------------------------------------------------------
 [{"@nodes":{"__identifiers" : ["1"], "nameEn" : "Vegetarian Meal Plan", "@person" : {"__identifiers" : ["3"], "fullName" : "User One"}}}]
(1 row)
```

Whereas if we run the explained SQL query of currentPerson, we get 0 rows as shown below.

```jsx
postgres=# select to_json((__local_0__."full_name")) as "fullName",
to_json((__local_0__."email")) as "email"
from "app"."current_person"( ) as __local_0__
where (
  not (__local_0__ is null)
) and (TRUE) and (TRUE)
postgres-# ;
 fullName | email
----------+-------
(0 rows)
```

This is because we have low level security implemented and it will not reveal the user because config is not set. So we need to set the jwt.claims.person_id within a transaction with set_config.

```sql
begin; -- start transaction
select set_config('jwt.claims.person_id', '1', true); -- set jwt claim
select to_json((__local_0__."full_name")) as "fullName",
to_json((__local_0__."email")) as "email"
from "app"."current_person"( ) as __local_0__
where (
  not (__local_0__ is null)
) and (TRUE) and (TRUE)
;
commit;
```

This gives a output when run in the psql prompt

```json
fullName |        email
----------+---------------------
 "Admin"  | "admin@example.com"
(1 row)
```

Postgraphile basically converts a graphQL query to a SQL query. It can do database access, HTTP Server and GraphQL schema management. Usually when we access the database from Node.js, we use ORM (Object Relational Mapper) libraries such as Prisma and HTTP router such as EXPRESS. But in Mealplanner, EXPRESS is used as a connect server only to open a connection and listen to the port and then we access the database from Node.js using Postgraphile. We are using Postgraphile because it directly implements complicated SQL queries that gives the output in JSON format via graphql.

Postgraphile writes functionalities to create (insert records), retrieve (read), update and delete records (known as CRUD operations) in tables. It also understands relations between tables which are one to one, one to many and many to one. It does not understand many to many relations. So we need to write a postgres function for postgraphile to understand many to many relations. 

It converts snake case table names and converts to camelCase fields such as meal_plan_entry to mealPlanEntry. It does inflection in English such as convert singular to plural for relationships such as mealPlanEntry to mealPlanEntries.

In `server.js` we use the `ConnectionFilterPlugin` to enable us to fiter on records with conditions (equivalent to WHERE in sql). But in order for the fields to be visible, you need to create an index on the column like so.

```jsx
create index app.idx_app_meal_plan_name_en on app.meal_plan(name_en);
```

This would allow `nameEn` to be used in the conditions section for the mealplans query or the mealplans connection.

```graphql
query displayMealPlans {
  mealPlans(condition: {nameEn: "Vegetarian Meal Plan", personId: "2"}) {
    nodes {
      id
      rowId
      nameEn
      personId
    }
  }
}
```

### Postgres

We always wrap our DDL (Data definition language) statements such as `CREATE TABLE` , `ALTER TABLE`, `CREATE TRIGGER`, etc., enclosed in transactions `begin`and `commit` . If you create a table and a trigger and the trigger creation fails, postgres will roll back the table created as well. This is not supported in some databases like Mariadb / MySQL. 

We use the `comment on` sql statement in our file instead of `-- comment` syntax to provide documentation to our graphql API.

The `bigserial` and `serial` datatypes in postgres also creates a sequence which provides the next_val for the id. When a user inserts a record the user needs `usage` permission to access the `next_val` of the sequence. So when we grant `insert` privilege for a user for the table, we need to ensure that we also grant the `usage` privilege on the associated sequence.

```jsx
grant usage on sequence app.nutrition_id_seq to app_meal_designer, app_admin;
grant insert, update, delete on table app.nutrition to app_meal_designer, app_admin;
```

### Polymorphic association

When a field in a table can refer to two different tables, it is called a polymorphic association. In our case, the `nutrition` table has `nutrionable_id` that can refer to both `meal(id)` or `product(id)` . It is not possible to directly create such a foreign key reference in while defining the table. So we need to create functions in both `product` and `meal` SQL scripts to associate the nutrition and the product or the nutrition and the meal. It takes product/meal as the argument and returns the nutrition object. This function is only required for postgraphile to create a relationship between the tables. 

```jsx
create or replace function app.product_nutrition(p app.product) returns app.nutrition as $$
  select * from app.nutrition n where n.nutritionable_id=p.id and n.nutritionable_type='product' limit 1;
$$ language sql stable;
comment on function app.product_nutrition(app.product) is 'Provides a link from Product to the specific nutritional value for the retail Product item, i.e. the nutritional label on the Product packaging.';
```

We can have functions of type `stable` or `volatile`. Functions marked stable should guarantee that no data changes while executing the function. Which means it is view only. In postgraphile we can access it only as a query and not as a mutation. The naming convention matters for the function. Only if you give it as `product_nutrition`, postgraphile will give nutrition under the product query. It follows the format `<table_name>_<custom_field>`.

```graphql
query product {
  products {
    nodes {
      nameEn
      nutrition {
        calories
        totalFat
        totalSugar
      }
    }
  }
}
```

By default, all functions are treated volatile. This means that functions can change the database while they execute. That means that they can do CRUD operations.

We need to provide the `execute` permission for the function to everyone whom we give `select` permission to. 

```jsx
grant execute on function app.product_nutrition(app.product) to app_anonymous, app_user, app_meal_designer, app_admin;
grant select on table app.product to app_anonymous, app_user, app_meal_designer, app_admin;
```

Postgres also allows you to create `enum` types that can restrict the content in a field. 

```jsx
create type app.category_t as enum('Breakfast', 'Lunch', 'Dinner', 'Snack');
```

Enums are a very space effective way of storing values as they only use 4 bytes on disk for value in a row. 

We create an index when a table has a foreign key reference. Usually for very small databases which will entirely fit into the size of RAM of the machine eg., 2 GB, we can skip creating indices. However, in practice, we may not be able to size the database well enough. Also creating an index after the fact when the table is pretty huge, it can cause performance issues. It is simpler to create indices while creating the table.

```jsx
create INDEX idx_measure_product_id ON app.measure(product_id);
create INDEX idx_measure_meal_id ON app.measure(meal_id);
```

Postgraphile does not automatically infer many-to-many relationships. We need to create a function to add the many-to-many relationship as a field. We need to ensure that we return a `SETOF` the record type as return value. Though it can also be returned as an array, it is best practice to use `SETOF` as Postgraphile can support pagination on the association such as filter, offset, first, last etc.

```jsx
CREATE or REPLACE FUNCTION app.product_meals(p app.product) RETURNS SETOF app.meal as $$
     SELECT m.* FROM app.meal m JOIN app.measure msr ON m.id = msr.meal_id
     WHERE msr.product_id=p.id;
$$ language SQL STABLE;
comment on function app.product_meals(app.product) is 'Provides a link between Product and the Meals in which it is included as an ingredient.';
```

### docker-compose.yml

There is docker-compose.yml file which lists all the services that are there such as db, graphql frontend and admin.

In docker-compose,

the db service, has the image postgres and says to bind the port 5432 to 5433 in our host machine so that we can access the postgres in the docker from our host machine in the port 5433

volumes basically specifies to create a hard disk virtually as pgdata which then is mounted inside the container at var/lib/postgresql/data

The .env has the POSTGRES_PASSWORD which postgres image in the docker needs.

the graphql service, the build context is mentioned as backend which means the dockercompose will look for the DockerFile cd ing into the backend folder.

exposes the port 4000

It refers to the .env file for JWT_SECRET for signing the cookie (backend → server.js uses this).

The graphql should start after the db, so we say depends_on: db, links: db

If we run psql from within the graphql container it will use the PG_HOST variable.

### DockerFile

In backend, you will find a DockerFile.

We need to install postgresql-client-12 (not postgres) and gettext-base for readline support (Ctrl+a, Ctrl+e, Ctrl+r, Ctrl+k, up arrow)

As node-18 does not have postgres12, we do the following in DockerFile

From the node-18 base image, we install postgresql client

We are creating pgdg.list file with deb from a particular url that refers bullseye-pgdg sub-folder 

Refer: https://www.postgresql.org/download/linux/ubuntu/

workdir basically does a mkdir and cd to app.

copying all contents of backend directory into app directory.

.dockerignore ignores node_modules

Then it installs dependencies in package.json for postgraphile

## Admin Interface:

`docker-compose up admin` to start the server. [http://127.0.0.1:2000/](http://127.0.0.1:2000/#/meals) will run. Use the same credentials of mealplanner


To get into the database for mealplanner:

```
docker-compose exec db psql -U postgres
```

To describe a table fields

```
postgres=# \d app.meal
```

```
select id, name_en, tags from app.meal
```

We are using the build tool Vite (similar to create-react-app’s webpack) https://vitejs.dev/guide/#scaffolding-your-first-vite-project

