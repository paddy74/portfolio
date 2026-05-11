# Data Dictionary

A data dictionary describes the structure, meaning, and constraints of data in a database or dataset.

## Example Data Dictionary

Below is an example of a data dictionary.

| Field Name  | Data Type | Length | Allow Nulls | Description                            | Example Value    |
| ----------- | --------- | ------ | ----------- | -------------------------------------- | ---------------- |
| customer_id | INT       |        | No          | Unique identifier for each customer    | 1023             |
| first_name  | VARCHAR   | 50     | No          | Customer's first name                  | John             |
| last_name   | VARCHAR   | 50     | No          | Customer's last name                   | Doe              |
| email       | VARCHAR   | 100    | No          | Customer's email address               | john@example.com |
| signup_date | DATE      |        | No          | Date the customer registered           | 2024-06-15       |
| is_active   | BOOLEAN   |        | No          | Whether the customer account is active | TRUE             |


## Example Data Dictionary Software

Here are some examples of open-source and paid tools that are or include a Data Dictionary:

1. Open-Source
   - Dataedo (Community Edition): Lets you document databases and export dictionaries to HTML/PDF.
   - dbdocs.io: Free online tool to generate and share database documentation.
   - SchemaSpy: Generates interactive database documentation from schema metadata.

2. Paid / Enterprise
   - Collibra: Enterprise-grade data governance and cataloging.
   - Alation: Data catalog with built-in dictionary and business glossary.
   - OvalEdge: Combines data catalog, dictionary, and governance features.

3. Built-in Database Features
   - SQL Server Management Studio (SSMS): Extended properties for columns/tables.
   - PostgreSQL COMMENT command: Store descriptions directly in the schema.
   - MySQL Workbench: Allows adding comments to schema objects.
