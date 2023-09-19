# Assignment 1

The goal of this assignment is to understand the HTTP REST protocol and how to use it in system integration.

## Requirements

You will be implementing a mini-reverse ETL application that can copy data from a data warehouse to SaaS applications. These are some reverse ETL tools available in the market.
* [Fivertran](https://www.fivetran.com/)
* [Hightouch](https://hightouch.com/)

### Data warehouse

We will use a Postgres DB as our data warehouse and will have this seed data.

* Create a new Customer database.

```sql
CREATE DATABASE customerdb;
```

* Create a customer table.
```sql
CREATE TABLE customer (
	customer_id serial PRIMARY KEY,
	first_name VARCHAR ( 50 ) UNIQUE NOT NULL,
	last_name VARCHAR ( 50 ) NOT NULL,
	email VARCHAR ( 255 ) UNIQUE NOT NULL,
	created_on TIMESTAMP NOT NULL,
        last_login TIMESTAMP 
);
```

### SaaS Application

On the SaaS application side, we will use [Google Sheets](https://developers.google.com/sheets/api/quickstart/python) as a SaaS application to transform data into.

## High-level Design



