# From Zero to Database Hero: A Beginner's Journey into SQL

## TOC
### [Introduction](#intro)
### [Database Key Terms](#keys)
### [SQL](#sql)
### [SQL Searches](#search)
### [Data Types](#types)
### [Insert, update, delete](#iud)
### [Solutions](#sol)


<a name="intro"></a>
## Introduction

![Server Room](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/y9508smkl98ur6w2836l.jpg)
Imagine you have a large collection of books in your personal library. Each book has a title, author, and other information such as publication year, genre, and publisher. If you wanted to find a specific book, you would need to manually search through each book until you found the one you were looking for. This process can be time-consuming and inefficient.

Now, imagine that you had a database of your book collection. The database would be structured in a way that makes it easy to search and update. Each book would be represented as a row in a table, with each column representing a different piece of information about the book. You could search for a book by title, author, or any other criteria, and the database would quickly retrieve the information you need.

**_A database is a structured set of data_**. It is structured in tables that are easy to search and update. By organizing data into tables and making it easy to search and update, databases help businesses make informed decisions, improve efficiency, and save time and money.

## Database Key Terms<a name="keys"></a>
![Database Keywords](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/hjq553bzuvh4kvh4l10h.png)

**A table** holds a collection of records for a particular theme in rows and columns. _Each row represents a single record or item_, and _each column represents a specific attribute or field_. 

Each **_record_** in the table needs a **_unique identifier_**. **_A primary key_** is used to give each record a unique code. A **_primary key_** can never be repeated. This ensures that each record in the table is unique. This is very important when dealing with thousands or even millions of records.

A **flat file database** is a database that contains a single table.

A **relational database** contains more than one table. The most common model for a database is a relational model. The data in the tables are linked using relationships. Relationships can be:   
- One to one

- One to many

- Many to many

In **relational database**, Data doesn’t need to be repeated and relationships can be made using the source table’s unique identifier. A primary key is unique to the original source of the data. 

When you link to a source table’s primary key you use a foreign key. **_A foreign key can be repeated because it is a link back to the primary key in the source table._**

## SQL <a name="sql"></a>

**SQL stands for Structured Query Language**. It is a language used to communicate with a database. You can use **SQL** to manipulate databases and retrieve records.
![SQL](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ogikbve1oj40jxgzg7l5.PNG) 

SQL is widely used. It is a standard language that comes in many varieties. The most popular are MySQL and SQLite. For this tutorial you will be using <a href="https://sqlitebrowser.org/blog/version-3-12-0-released/">SQLite</a>.

SQL uses recognisable commands that are similar to the English language, making it easy for users to write and understand queries. 

The commands used in SQL are called keywords, and they are used to perform various operations on a database, such as creating tables, inserting data, updating records, and retrieving information. 

Some of the most commonly used SQL keywords include **SELECT, FROM, WHERE, INSERT, UPDATE, and DELETE**. These keywords are designed to be intuitive and easy to understand, even for those who are not familiar with programming or database management.

For example when you shop for items online you will typically be searching a database that uses SQL. Your search terms will be added to SQL statements and the relevant records will be retrieved from the database. 

A SELECT query could be used to retrieve data from the database.
- SELECT the item, price and description columns.

- FROM the tblProducts table.

- WHERE the criteria has been met

```sql
SELECT item, price, description 
FROM tblProducts 
WHERE keyword = "toy";
```

## SQL Searches <a name="search"></a>
After installing <a href="https://sqlitebrowser.org/blog/version-3-12-0-released/">SQLite</a>, download and open <a href="https://drive.google.com/file/d/1pbBQPClSyE_FR4k_8YK3nlSpqaWePmwO/view?usp=share_link">dbMusic</a>. Then Complete the following activities.

- 
Explore a Database
<a href="https://docs.google.com/document/d/1yjM7Hl6Qd9Cfs4XgZ1UEuIdGEo2B3DoX/edit?usp=share_link&ouid=117248931667314197495&rtpof=true&sd=true">A3 Worksheet</a>.

- 
Retrieving Data with SQL
<a href="https://docs.google.com/document/d/1d4DADhxurvl1BltbqeM0-j_ZI96A4Scy/edit?usp=share_link&ouid=117248931667314197495&rtpof=true&sd=true">A1 Worksheet</a>.

- Retrieving data from more than one table 
<a href="https://docs.google.com/document/d/1gnm0ihpSG39sbe5dyC818tPW4fzkDBwn/edit?usp=share_link&ouid=117248931667314197495&rtpof=true&sd=true">A2 Worksheet</a>

## Data Types <a name="types"></a>
**Fields** in a database (as with variables in a programming language) have data types associated with them. _Data types specify the type of value the field can hold_. 

**MySQL and SQLite** are both relational database management systems that provide different data types to define the type of data that can be stored in a field.
![Data Types](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/164kmwzyuu1ymkc9wl7k.PNG)
For example, _MySQL provides data types like INT, VARCHAR, TEXT, DATE,_ etc., while _SQLite provides data types like INTEGER, TEXT, REAL,_ etc.
![Data Types](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7wkdn57f06yc6zlynik2.PNG)
In conclusion, data types are essential elements in any database that define the type of data that can be stored in a particular field. Choosing the appropriate data type for each field is crucial to ensure the accuracy and consistency of data stored in the database.

![Data Types](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/9wxsi9wj49cvks2v7yl2.PNG) With the wide range of data types available in database management systems like MySQL and SQLite, developers can create more robust and efficient databases capable of handling various types of data.

## Insert, update, delete <a name="iud"></a>
**Insert, update, and delete** are the three fundamental operations in database management used to add, modify, and remove data. They are crucial for maintaining database integrity and accuracy.

### Inserting data
An **SQL INSERT** statement allows you to add data into pre-existing tables. 

The statement allows you to specify: 
- The table which you intend to insert data into. 
- Which fields to use. 
- Which VALUES to enter into those fields.

```sql
INSERT INTO tblFriends (firstname,surname) 
VALUES(“Rachel”, “Green”), (“Phoebe”,”Buffay”),(“Chandler”, “Bing”);
```

```sql
INSERT INTO tblMembers (Firstname,Surname, Email, Password)
VALUES(“Nicole”, “Battle”,”Nbat@mail.com”,”Nr5@Wd”);
```

### Updating Data
An **SQL UPDATE** statement allows you to amend existing records in tables.

To update data in a table, you are required to specify the following: 
- The table which you intend to UPDATE 
- The new value that you want to SET 
- WHERE a condition is being met

```sql
UPDATE tblUsers 
SET Firstname = “James” 
WHERE userid = 8;
```
### Deleting Data
An SQL DELETE statement allows you to remove existing records from a table.

To delete data from a table, you are required to specify the following:
- The table which you intend to DELETE FROM 
- WHERE a condition is being met

```sql
DELETE FROM tblStudents 
WHERE date_of_birth < 31/08/2002;
```



### Solutions: <a name="sol"></a>
<a href="https://docs.google.com/document/d/1mQOVEpYZ9fnuavjv-2rUC2P5GJxAjOo7/edit?usp=share_link&ouid=117248931667314197495&rtpof=true&sd=true">Explore a Database Solutions</a>

<a href="https://docs.google.com/document/d/1sDz9SUMzzSg7QD5GBoHJl5rGM4nREb52/edit?usp=share_link&ouid=117248931667314197495&rtpof=true&sd=true">Retrieving Data with SQL Worksheet Solutions</a>

<a href="https://docs.google.com/document/d/1dnxF_0DBbHa2XfcL1ixC2ZSSDVa1Vjab/edit?usp=share_link&ouid=117248931667314197495&rtpof=true&sd=true">Retrieving data from more than one table Solutions</a>



















