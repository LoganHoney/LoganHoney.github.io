---
layout: post
title: SQL Interview Prep
subtitle: "Real SQL Skills for Real Interviews—No Filler, Just What Matters"
description: "Ace your next data job interview with this comprehensive SQL prep guide—covering real-world questions, efficient query patterns, joins, subqueries, and optimization tips."
cover-img: /assets/img/4173705.jpg
share-img: /assets/img/4173705.jpg
tags: [sql, interview, prep, data]
slug: "sql-interview-prep"
author: Logan Honey

---
# Not sure where to start? Perfect.
Whether you are new to the data field, refreshing yourself before the interview, or you are just scratching that curiosity itch. I hope tp provide you with some thoughts you can take with you. We're going to cover the basics of SQL as well as a few easy-to-implement advanced skills. After all, we need to stand out and showcase our potential. The basics of SQL are incredibly easy to grasp and they lay the foundation for your career in Data. 

## The Basics
SQL stands for **_Structured Query Language_**. It is a language used to update, create, maintain, and query databases. At the most besic deconstruction, there are three fundamental concepts found in every query:

```sql
SELECT (Data)
FROM (Table)
WHERE (Condition)
```
#### SELECT
The first word in nearly every query. `SELECT` is where we tell the database what columns to retrieve. It is also here that we often put the finishing touches on our query such as minor data manipulation and renaming columns. Personally, I do not _primarily_ focus on `SELECT` at first unless I am familiar with the particular table I am querying from. Although it is necesary, it is not my focus. This will make better sense in a second, I promise. 

#### FROM
We should already have a basic understanding of what we are trying to accomplish with our query. However, we may not always know where to start. Thus begins the quest of searching for data. If you've done this, congratulations! You are now a data digger. In my experience, this step is often times the longest as it involves trial and error and using your judgment as to which table(s) are best to produce your desired outcome. I've found a few helpful tricks to help dig for data and we'll cover them in the **_Tips & Tricks_** section. For now, `FROM` is the section where we specify from which table to query. We will also tack on other tables as the complexity of the query expands using `JOIN`.

#### WHERE
This is **_where_** the magic happens. Any criteria that we want to constrain or filter the data by is specified in the WHERE clause. For example, if I want to find the first names of everyone in accounting, my query may look something like this:
```sql
SELECT firstName
FROM Employee
WHERE Department = 'Accounting'
```
Or if I need to find the first and last names of all employees who were hired after a specific date:
```sql
SELECT firstName, lastName
FROM Employee
WHERE HireDate > '01/12/1998'
```
The ability to use `WHERE` effectively will add incredible power to the value you can provide an organizaion. 

## Interpretation
One key factor that sets you apart from others isn't even SQL realted but rather interpersonal. Your ability to interpret needs and communicate effectively will mkae or break your career potential. In my experience, a significant portion of requests for new or updated reports comes from non-technical users who may struggle to articulate their needs.

To excel in any role, focus on the following:

- **Ask Thorough Questions:** Engage with users to clarify their requests and understand their underlying needs.
- **Translate Requests into Actionable Steps:** Convert vague requests into clear, actionable tasks that you can execute.
  
By bridging the gap between end-users and development, you will position yourself as a more valuable candidate or employee. Remember, SQL is a development language, but effective communication is what truly drives successful outcomes.

## Tips & Tricks
Below are some helful tips and tricks that I have used over my career. They range from very basic to more advanced. I can assure that each one has a particular use-case in which it will shine and not one-size-fits-all, **_but it may get you close._**

#### Select *
```sql
SELECT *
FROM (Table)
```
This is one of the first and simplest tricks I learned and I still use it everytime I am building queries. This goes back to what I said previously about not primarily focusing on `SELECT`. More often than not, finding the data is the most important aspect of any data role. Using `SELECT *` allows me to grab all columns of a table. By doing this I can quickly see if this table is one that can help me achieve whatever goal I am trying to achieve. If I were looking for emloyee addresses:

This: 
```sql
SELECT *
FROM Employee
```
Yields:

| ID | firstName | lastName | Email | Salary | Address |
|----|--------|-------|-------|------|-----|
|  1 | John | Doe | jdoe@email.com | 60k | 123 Maple St.|


#### Select TOP 1000
```sql
SELECT TOP (1000)
FROM (Table)
```
#### Script View

#### View Dependencies of Tables and Views
