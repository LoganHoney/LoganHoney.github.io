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
From healthcare to fast food, the supply chain to your local coffe shop, data is instrumental in providing the insights needed to succesfully manage any insitution. Let's take a look at a few qualities that giver them their power.

### Structured Storage
Not only do relational databases store vast amounts of data, data is also stored efficiently. Relational databases use tables to organize data into rows and columns. This structured format allows for:

- **Clear Relationships**: Data can be easily related through foreign keys, enabling complex queries across multiple tables.
- **Data Integrity**: Constraints (like primary keys and foreign keys) ensure that the data remains accurate and consistent.

### Connected Data
All data in these databases are connected or **_related_**. How this is done is through the aforementioned **_foreign keys_**. A foreign key can be defined as a field that exsists in more than one table. This alows all of the data in both tables to be tied together. This is the driving force between a relational database's power. I believe that an example would be of benefit:

##### Customer Table

| Customer_ID | First_Name | Last_Name | Street | City | State | Zip |
| :---- | :--- | :--- | :--- | :--- | :--- | :--- |
| 01 | Wallace | Cleaver | 211 Pine St | Mayfield | OH | 12345 |
| 02 | Michael | Scott | 473 Apple Ln | Scranton | PA | 16754 |
| 03 | Ray | Barone | 647 Robin Dr | New York | NY | 21257 |

#### Orders Table

| Order_ID | Customer_ID | Item | Color | Quantity | Unit Price |
| :--------| :--- | :--- | :--- | :--- | :--- |
| 1457 | 03 | Desk Chair | Black | 1 | $250 |
| 1458 | 01 | Fountain Pens | Blue | 5 | $1 |
| 1459 | 02 | Coffee Mug | White | 2 | $10 |

With these table being linked by **_Customer_ID_**, it can easily be see which customer placed which order. This allows for fast transactions and ensures that the customers receive the products that they ordered. 



