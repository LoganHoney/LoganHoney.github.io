---
layout: post
title: SQL Interview Prep
subtitle: "Real SQL Skills for Real Interviews—No Filler, Just What Matters"
description: "Ace your next data job interview with this comprehensive SQL prep guide—covering real-world questions, efficient query patterns, joins, subqueries, and optimization tips."
cover-img: /assets/img/SQLtables.jpg
share-img: /assets/img/SQLtables.jpg
tags: [sql, interview, prep, data]
slug: "sql-interview-prep"
author: Logan Honey

---
# Not sure where to start? Perfect.
Whether you are new to the field or you are just refreshing yourself before the interview, I know there is something here for you. We're going to cover the basics as well as a few easy-to-implement advanced skills. After all, we need to stand out and showcase our potential. Let's get started.

## The Basics
SQL stands for Structured Query Language. As such, understanding these basic building blocks lays the foundation to build complex queries. Here are the three fundamental concepts of every query:

```sql
SELECT (Data)
FROM (Table)
WHERE (Condition)
```
#### SELECT
The first word in nearly every query. SELECT is where we tell the database what data to retrieve. It is also here that we often put the finishing touches on our query such as minor data manipulation. Personally, I do not primarily focus on SELECT at first unless I am familiar with the particular table I am querying from. Although it is necesary, it is not my focus. This will make better sense in a second, I promise.

#### FROM
We should already have a basic understanding of what we are trying to accomplish with our query. However, we may not always know where to start. Thus begins the quest of searching for data. If you've done this, congratulations! You are now a data digger. In my experience, this step is often times the longest as it is a lot of trial and error and using your judgment as to which table(s) are best to produce your desired outcome. I've found a few helpful tricks to help dig for data and we'll cover them in the **_Tips & Tricks_** section.

#### WHERE
This is _where_ the magic happens. Any criteria that we want to constrain or filter the data by is specified in the WHERE clause. For example, if I want to find the first names of everyone in accounting, my query may look something like this:
```sql
SELECT firstname
FROM Employee
WHERE Department = 'Accounting'
```

## Interpretation
One huge factor that will set you apart from others is your ability to interperet. No I'm not talking interpreting a spoken language but instead a written one. In my experience, a decent portion of the request for new reports or updated reports comes from the non-technical user who does not always know how to say what they want. Your ability to ask thorough questions and turn their request into actionable steps on your part will make you a much more prospective candidate than someone who just knows how to query but cannot effectively bridge between end users and development. After all, SQL is a development language.
## Tips & Tricks

#### Select *
```sql
SELECT *
FROM (Table)
```
#### Select TOP 1000
```sql
SELECT TOP (1000)
FROM (Table)
```
#### Script View

#### View Dependencies of Tables and Views
