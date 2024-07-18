# Hands-on-Project-INSERT-UPDATE-DELETE
In this project, I demonstrated skills writing DML (Data Manipulation Language) statements of SQL such as:
1. The INSERT statement, which is used to insert new rows into a table.
2. The UPDATE statement, which is used to update the data in existing rows in the table.
3. The DELETE statement, which is used to remove rows from a table.

# Objectives
The objectives of this project are to demonstrate skill in writing SQL statements to:
1. Insert new rows into a table
2. Update data in existing rows of the table
3. Remove rows from a table

# Highlights

- How does the syntax of an INSERT statement look?

INSERT INTO table_name (column1, column2, ... )
VALUES (value1, value2, ... )
;

- How does the syntax of an UPDATE statement look?

UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition
;

- How does the syntax of a DELETE statement look?

DELETE FROM table_name
WHERE condition
;

# Software Used in this Project
In this project, I used PgAdmin 4 (PostgreSQL 15)

# Project Phases
The project was conducted in Four (4) phases as detailed below:

# Phase 1: Creating the Instructor Table in PgAdmin

- Step 1: Creating a new database 

1. I opened PgAdmin on my local computer and connected to my PostgreSQL server,
2. Right-clicked on the "Databases" node in the Browser panel on the left-hand side,
3. Selected "Create" > "Database",
4. In the "New Database" window:
   a. I entered the name of my database, "Instructor", 
   b. Selected the owner (usually your PostgreSQL username, e.g., ELITEBOOK 840),
   C. Clicked "Save" to create the database.

- Step 2: Creating a new table called Instructor

1. I navigated to my new database named "Instructor":
   a. Expanded the "Databases" node,
   b. Expanded the "Instructor" node,
2. Right-clicked on the "Tables" node under my new database,
3. Selected "Create" > "Table",
4. In the "Create - Table" window:
   a. I entered the name of my table, "Instructor",
   b. Navigated to the "Columns" tab,
5. Added columns to your table:
   a. Clicked the "+" button to add a new column.
   b. For each column, I entered the name and selected the data type as follows:
 (ins_id integer
lastname character(20)
firstname character(20)
city(20)
country (2))
   C. Repeated for all columns as defined below:
7. Clicked "Save" to create the table.

# Phase 2: Inserting rows into the Instructor table.

I populated the Instructor table using the following INSERT statement

INSERT INTO "Instructor" (ins_id, lastname, firstname, city, country)
VALUES(1, 'Ahuja', 'Rav', 'Toronto', 'CA'),
	  (2, 'Chong', 'Raul', 'Toronto', 'CA'),
	  (3, 'Vasudevan', 'Hima', 'Chicago', 'US'),
	  (4, 'Saha', 'Sandip', 'Edmonton', 'CA'),
	  (5, 'Doe', 'John', 'Sydney', 'AU'),
	  (6, 'Doe', 'Jane', 'Dhaka', 'BD'),
   7, 'Cangiano', 'Antonio', 'Vancouver', 'CA'),
	(8, 'Ryan', 'Steve', 'Barlby', 'GB'), 
	(9, 'Sannareddy', 'Ramesh', 'Hyderabad', 'IN');

SELECT * FROM "Instructor"

![image](https://github.com/user-attachments/assets/20ae9d5b-8c6f-4f83-bb95-b3d67ee69670)

# Phase 3: Updating some values in the Instructor table.

I updated some values in the Instructor table using the following UPDATE statements

- Updating the city for Sandip to Toronto.

UPDATE "Instructor"
SET city= 'Toronto' 
WHERE firstname= 'Sandip';

SELECT * FROM "Instructor"

![image](https://github.com/user-attachments/assets/789fa602-db1a-4b6d-9cee-11bcf2f4c2dd)

- Update the city and country for Doe with id 5 to Dubai and AE respectively.

UPDATE "Instructor" 
SET city= 'Dubai', country='AE' 
WHERE ins_id=5 AND lastname = 'Doe';

SELECT * FROM "Instructor"

![image](https://github.com/user-attachments/assets/01e8ba02-409f-4847-bcce-4dd4dd35d01f)

- Update the city of the instructor record to Markham whose id is 1.

UPDATE "Instructor"
SET city = 'Markham'
WHERE ins_id = 1

SELECT * FROM "Instructor"

![image](https://github.com/user-attachments/assets/af039ce0-619d-4201-953a-1cb95a83ff46)

- Update the city and country for Sandip with id 4 to Dhaka and BD respectively.

UPDATE "Instructor"
SET city = 'Dhaka', country = 'BD'
WHERE ins_id = 4;

SELECT * FROM "Instructor"

![image](https://github.com/user-attachments/assets/dbb16fee-1a48-4d85-a1d6-3f760c246cc8)

# Phase 4:  Deleting some records from the Instructor table.

- Remove the instructor record of Doe whose id is 6.

DELETE FROM "Instructor"
WHERE ins_id = 6 AND lastname = 'Doe';

SELECT * FROM "Instructor"
ORDER BY ins_id ASC

![image](https://github.com/user-attachments/assets/c4140de5-6598-47da-a0f3-b98c42747d6b)

- Remove the instructor record of Hima.

DELETE FROM "Instructor"
WHERE firstname = 'Hima';

SELECT * FROM "Instructor"
ORDER BY ins_id ASC

![image](https://github.com/user-attachments/assets/80e61958-84b6-423d-8f25-ad0daa36c6f4)










