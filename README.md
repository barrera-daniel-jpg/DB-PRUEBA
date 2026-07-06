# DB-PRUEBA

## Module 4 Database Test Deliverable
### Project Description
This documentation outlines the criteria and technologies used to solve the problems identified. Therefore, all of the above, along with other parameters used in the test, will be detailed below.

### Technologies used.

The technologies and tools used were:
- Docker Desktop
- PostgreSQL and its graphical interface pgAdmin4
- Draw.io for creating the ER model
- LibreOffice Writer
- GitHub

### Database engine used.
An SQL database was implemented because the recorded data contains a correlation between the entities present, such as the warehouse in relation to its location.

### Explanation of normalization process.
The three normal forms were applied to create an optimal database, which prevents inconsistencies from arising in future data entry scenarios.

### Entity Relationship Model.
<img width="1386" height="871" alt="Diagrama" src="https://github.com/user-attachments/assets/82701401-ebf2-410b-8a69-f4c775bbd1e2" />


Instructions to create the database.
A database named "bd_daniel_barrera_magdalena" was created within the graphical interface so that tables could be inserted and more information added within them using DDL and DML scripts.

### Video Route

/home/Cohorte5/Vídeos/Grabaciones de la pantalla/
---

### 1. ANALYSIS AND NORMALIZATION
1- The initial structure is an unnormalized Excel file.

2- After analyzing the provided Excel file, several inconsistencies were identified, such as:
- Duplicate suppliers with different formatting.
- Repeated categories.
- Cities spelled differently.
- Products with inconsistent names.
- Redundant fields.
- Attributes that create dependencies.
- Data within repeated, incomplete, or poorly structured categories.

- Suppliers registered multiple times with different names.

- Duplicate products or products with inconsistent descriptions.

- Warehouses registered with duplicate information.

- Difficulty generating reliable reports.

Within the established parameters for building an optimal database, these inconsistencies can create complete chaos when designing a robust database; therefore, the proper process is applied to eliminate all these inconsistencies. 3. Following step 2, several entities with unique attributes were created to eliminate redundancy and inconsistency in current and future data, adhering to the principles of the first three normal forms (atomicity of values, elimination of partial dependencies, and elimination of transitive dependencies).
The final result is entities with optimal cardinalities for large amounts of data, without the inconsistencies evident in the initial Excel file.

### Scrip DDL para la creacion de las tablas
CREATE TABLE riwi_supplier (
id SERIAL PRIMARY KEY,
name VARCHAR (100)

);

CREATE TABLE riwi_city (
id SERIAL PRIMARY KEY,
name VARCHAR (100)

);

CREATE TABLE riwi_warehouse (
id SERIAL PRIMARY KEY,
name VARCHAR (100)

);

CREATE TABLE riwi_category (
id SERIAL PRIMARY KEY,
name VARCHAR (100)

);

CREATE TABLE riwi_product (
id SERIAL PRIMARY KEY,
name VARCHAR (100)


);

CREATE TABLE riwi_puerchase_order (
id SERIAL PRIMARY KEY,
name VARCHAR (100)

);


### Scrip DML para instar datos a una tabla especifica
(Instar daots en la table riwi_city)

INSERT INTO riwi_city (id, name)
VALUES ('1','Barranquilla');

INSERT INTO riwi_city (id, name)
VALUES ('2','Cartagena');

INSERT INTO riwi_city (id, name)
VALUES ('3','Santa Marta');


Scrip para insertar datos a la tabla riwi_category:

INSERT INTO riwi_category (id, name)
VALUES ('1','Herramientas');

INSERT INTO riwi_category (id, name)
VALUES ('2','Consumibles');

INSERT INTO riwi_category (id, name)
VALUES ('4','EPP');

INSERT INTO riwi_category (id, name)
VALUES ('5','Elementos de proteccion');

