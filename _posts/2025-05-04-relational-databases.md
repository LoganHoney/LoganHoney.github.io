---
layout: post
title: Relational Databases 
subtitle: A closer look at what makes them powerful
cover-img: /assets/img/SQLtables.jpg
share-img: /assets/img/SQLtables.jpg
tags: [sql, relational databses, data]
auhtor: Logan Honey
---

## What are relational databases?
From healthcare to fast food, the supply chain to your local coffe shop, data is instrumental in providing the insights needed to succesfully manage any insitution. Let's take a look at a few qualities that give relational databases their power.

### Structured Storage
Not only do relational databases store vast amounts of data, data is also stored efficiently. Relational databases use tables to organize data into rows and columns. This structured format allows for:

- **Clear Relationships**: Data can be easily related through foreign keys, enabling complex queries across multiple tables.
- **Data Integrity**: Constraints (like primary keys and foreign keys) ensure that the data remains accurate and consistent.

#### Clear Relationships
All data in these databases are connected or **_related_**. How this is done is through the aforementioned **_foreign keys_**. A foreign key can be defined as a field that exsists in more than one table. This alows all of the data in both tables to be tied together. This is the driving force between a relational database's power. I believe that an example would be of benefit:

###### Customer Table

![CustomerTable](https://loganhoney.github.io/assets/img/customerstable.png)


###### Orders Table

![OrdersTable](https://loganhoney.github.io/assets/img/orderstable.png)


By linking these tables through **_C_ID_**, it becomes clear which customer placed each order. This facilitates quick transactions and ensures that customers receive the products they ordered. Consider the potential applications; this concept extends beyond just customers and orders.

- **Health Insurance:** It can track which claims have been submitted by an individual.
- **Entertainment:** It can be used to identify what movies have been purchased through an individuals Netflix account.
- **Inventory Management:** It can be  used with a barcode system and monitor the quantity of products on the shelves and determine when it needs to be restocked.
- **Education:** It can associate students with their course enrollments and grades, helping to track academic progress.

Here is an example of structure using a small database:

![DatabaseExample](https://loganhoney.github.io/assets/img/empdatabase.png)

#### Data Integrity
How important is good information? In business, the smallest details can influnce big decisions. Decisions made off of inconsistent data can be have wildly unintended results. That's why we must preserve data integrity with good database management skills. This can be achieved through proper use of **primary keys**, **foreign keys**, and **Data Validation**

###### Primary Keys
Data integrity is maintained through the use of primary keys. These keys are typically system-generated rather than user-defined, as they must be unique to prevent duplication. Each piece of information in a table is linked to a primary key. For instance, consider a Driver License Number or Social Security Number; both of these identifiers must be unique, and various data points are associated with them.

Here’s an example of a table that illustrates this concept: 

![DogTable](https://loganhoney.github.io/assets/img/dogtable.png)


The **_Tag#_** is the primary key because it is unique and cannot be duplicated. In this table there are two **Beagles** named **Fido** that are **Brown/White** and **1.5** years old. In every way, these dogs are identical except for their **_Tag#_**. This unique number allows the two dogs to be distinguished from one another in the database. Now any information such as vaccines, medications, or the kennel they are in can be linked to the **_Tag#_** and not just the name or breed. The point is, each row in a table must have a unique identifier to maintain data integrity. 

###### Foreign Keys
Foreign keys already play a vital role in the power of any relational database (It's kind of what they're known for). 


###### Data Validation

Another way that relational databases maintain data integrity is through **Data Validation**.Data Validation or **_Domain Integrity_** involves defining valid values for a column, such as data types, formats, and ranges. Constraints like CHECK constraints ensure that only valid data is entered. Below is an example:
``` sql
CREATE TABLE Users (
    UserID INT PRIMARY KEY,
    UserName VARCHAR(50) NOT NULL,
    Age INT CHECK (Age > 10)
);
```


This `CREATE TABLE` statement demonstrates several aspects of domain integrity.
- It specifies **_UserID_** as the primary key (by default, unabe to be a NULL Value)
- It specifies **_UserName_** as a variable character field with a maximum of 50 characters that cannot be NULL
- It specifies **_Age_** as an integer and CHECKS to make sure that the user is older than 10.

If a number of 10 or less is entered into the **_Age_** field, you would receive an error similar to:
`ERROR: new row for relation "Users" violates check constraint "Users_Age_check"`

  


