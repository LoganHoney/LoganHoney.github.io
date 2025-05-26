---
layout: post
title: Relational Databases 
subtitle: A closer look at what makes them powerful
cover-img: /assets/img/SQLtables.jpg
share-img: /assets/img/SQLtables.jpg
tags: [sql, relational databases, data]
author: Logan Honey
{% include reading-time.html %}
---

## What are relational databases?

From healthcare to fast food, the supply chain to your local coffee shop, data is instrumental in providing the insights needed to successfully manage any institution. Let's take a look at a few qualities that give relational databases their power.

### Structured Storage

Not only do relational databases store vast amounts of data, they also store it efficiently. Relational databases use tables to organize data into rows and columns. This structured format allows for:

- **Clear Relationships**: Data can be easily related through foreign keys, enabling complex queries across multiple tables.
- **Data Integrity**: Constraints (like primary keys and foreign keys) ensure that the data remains accurate and consistent.

#### Clear Relationships

All data in these databases is connected or **_related_**. This is achieved through the use of **_foreign keys_**. A foreign key is a field in one table that references the primary key in another. This relationship ties the data together and is one of the core strengths of a relational database.

###### Customer Table

![CustomerTable](https://loganhoney.github.io/assets/img/customerstable.png)

###### Orders Table

![OrdersTable](https://loganhoney.github.io/assets/img/orderstable.png)

By linking these tables through **_C_ID_**, it becomes clear which customer placed each order. This facilitates quick transactions and ensures that customers receive the products they ordered.

Consider the broader applications — this concept extends beyond just customers and orders:

- **Health Insurance:** Track which claims have been submitted by an individual.
- **Entertainment:** Identify what movies have been purchased through a user’s Netflix account.
- **Inventory Management:** Monitor the quantity of products on the shelves and determine when restocking is needed.
- **Education:** Associate students with their course enrollments and grades to help track academic progress.

Here is an example of structure using a small database:

![DatabaseExample](https://loganhoney.github.io/assets/img/empdatabase.png)

---

### Data Integrity

How important is good information? In business, the smallest details can influence big decisions. Decisions made based on inconsistent data can lead to wildly unintended results. That’s why we must preserve data integrity with good database management practices. This is achieved through proper use of **primary keys**, **foreign keys**, and **data validation**.

###### Primary Keys

Data integrity is maintained through the use of **primary keys**. These keys are typically system-generated rather than user-defined and must be unique to prevent duplication. Each row in a table is associated with a primary key.

For example, consider a driver's license number or social security number. Both must be unique, and various data points can be reliably associated with them.

Here’s a visual example:

![DogTable](https://loganhoney.github.io/assets/img/dogtable.png)

The **_Tag#_** is the primary key because it is unique and cannot be duplicated. In this table, there are two **Beagles** named **Fido** that are **Brown/White** and **1.5** years old. These dogs are identical in every way except for their **_Tag#_**. This unique identifier distinguishes the two entries. Any information such as vaccines, medications, or kennel location can now be linked to the **_Tag#_** rather than relying on the name or breed.

The key takeaway: each row in a table must have a unique identifier to maintain data integrity.

###### Foreign Keys

Foreign keys connect tables by referencing a primary key in another table. This not only builds relationships but also ensures that data is consistent across the database — a foreign key must match an existing primary key in the referenced table. This ensures that, for example, orders cannot be linked to customers that do not exist.

###### Data Validation

Another way that relational databases maintain data integrity is through **data validation**. **_Domain integrity_** involves defining valid values for a column, such as data types, formats, and acceptable ranges. Constraints like `CHECK` ensure that only valid data is entered.

Below is an example:

```sql
CREATE TABLE Users (
    UserID INT PRIMARY KEY,
    UserName VARCHAR(50) NOT NULL,
    Age INT CHECK (Age > 10)
);
```


This `CREATE TABLE` statement demonstrates several aspects of domain integrity.
It specifies **_UserID_** as the primary key (which cannot be NULL and must be unique).
It defines **_UserName_** as a variable character field with a maximum of 50 characters that cannot be NULL.
It ensures **_Age_** is an integer and must be greater than 10.

If a value of 10 or less is entered into the **_Age_** field, the system will return an error similar to:
`ERROR: new row for relation "Users" violates check constraint "Users_Age_check"`

### Final Thoughts

In today's data-driven world, the accuracy and consistency of information isn't just a technical concern — it's a business imperative. From customer transactions to medical records, even the smallest error can have far-reaching consequences. That’s why **data integrity** isn’t optional; it’s essential.

<div class="callout warning">
  <strong>⚠️ Why It Matters:</strong> Without data integrity, even the most advanced systems will produce unreliable results. Errors compound quickly, and decisions made on bad data can cost money, time, or trust.
</div>

Relational databases are purpose-built to ensure that the data you rely on is not only well-organized but also trustworthy and verifiable. Through structured tables, defined relationships, and enforced validation rules, relational databases provide the backbone for reliable decision-making. Whether you're managing inventory, tracking student performance, or processing insurance claims, relational databases check every box — offering clarity, scalability, and most importantly, **integrity**. When your data is accurate, your insights are sharper, your systems more efficient, and your outcomes far more predictable.



