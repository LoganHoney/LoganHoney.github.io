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

##### Customer Table

| **Customer_ID** | First_Name | Last_Name | Street | City | State | Zip |
| :---- | :--- | :--- | :--- | :--- | :--- | :--- |
| 01 | Wallace | Cleaver | 211 Pine St | Mayfield | OH | 12345 |
| 02 | Michael | Scott | 473 Apple Ln | Scranton | PA | 16754 |
| 03 | Ray | Barone | 647 Robin Dr | New York | NY | 21257 |

##### Orders Table

| Order_ID | **Customer_ID** | Item | Color | Quantity | Unit Price |
| :--------| :--- | :--- | :--- | :--- | :--- |
| 1457 | 03 | Desk Chair | Black | 1 | $250 |
| 1458 | 01 | Fountain Pens | Blue | 5 | $1 |
| 1459 | 02 | Coffee Mug | White | 2 | $10 |

With these table being linked by **_Customer_ID_**, it can easily be seen which customer placed which order. This allows for fast transactions and ensures that the customers receive the products that they ordered. Think about the possibilities, this doesn't just apply to customers and orders. It could apply to any number of systems or buisiness models. Health Insurance: Which claims have been filed by an individual. Entertainment: What email account was used to create a Netflix account. Inventory: How much of a certain product is on the shelves and when does it need to be restocked. 

#### Data Integrity

Data integrity is preserved by using **primary keys**. Primary keys are often system generated and not user defined because it must be unique (no duplication) All information in any given table is associated with a primary key. For example: Driver License Number and Social Security Number. These two numbers cannot be duplicated and many pieces of information are connected to them. 

| Driver License Number | First_Name | Last_Name | DOB | Height | Gender | Address |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| D500-000-000 | John | Doe | 05/13/1995 | 5'10" | M | 123 Maple Dr. |

The driver license number is the primary key because it is unique and cannot be duplicated. There could be multiple individuals with the name of John Doe. There could be multiple people born on 05/13/1995. There could also be multiple people living at 123 Maple St. 


