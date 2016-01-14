# Intro to SQL

Here are notes on learning some SQL basics. This file is the chapter 0 / syllabus.

## Installation

Download the Postgres version of Navicat -- the program we'll use to run SQL.

http://www.navicat.com/download/navicat-essentials

I'll give instructions on how to connct to the databases in Slack

## What's it all about?

Imagine you go to the dentist's office, and have to fill out an insurance form. 
How do you store and organize the forms so it's easy to access them them later?

- Your filled-out form will go in a big filing cabinet
- It's going to go in the drawer labeled "Insurance forms"
- The drawer is filled with records of peoples' insurance information
- The format of every form in that drawer is the same: 
    Name (text), address (text), date of birth (date), provider (text), ...
- Your form will be separated by manilla folders/dividers labeled with the first letter of your last name. 
    Each drawer will have a bunch of manilla folders/dividers
    This makes it easier for the receptionist to find your form next time you visit.

Databases solve the same sort of organizational problem for many kinds of electronic data:

- A **database** is a place to store a bunch of data. The filing cabinet
- A **table** is a table of data, just like in Excel. A drawer of the cabinet
- A **record** is a row in a table. An individual form
- A **schema** describes the data in each row of the table. The structure of the insurance form
- An **index** is a tool for organizing records. The manilla divider

**SQL** is code used to wrangle data stored in databases.
You use it to ask questions about the data. Hence, chunks of SQL code are called **queries**.

There are lots of different types of SQL: They're all basically the same, with some differences in what they're best used for, and bonus featues they have.

## Why is SQL useful?

It provides a simple way to ask questions from the data you have available.
By simple, I mean that compared to other programming languages, it's pretty easy to learn the basics.
**Therefore it can empower many people within an organization to encorporate data into their business decision making.**

However, learning to do advanced things, or ask complicated questions of your data with SQL takes practice.
One should also consider when making decisions based on data: Your insights are only as valid as the underlying data.
Therefore you should often consult with other analysts and inspect your data before encorporating it into your decision making.

## Where does data come from?

Some simple examples are:
1. Your website has a signup form that asks for the users name, email adress, and phone number.
    Everytime someone submits the form on your site, the data will be put into a row of a table. Each row might tell you
  - datetime the form was submitted
  - the users name
  - email address
  - phone number
2. Everytime someone clicks on your website, a row in a table is populated. In that row it could tell you
  - the id of the user (if your site has user ids)
  - datetime of the click
  - what page of they website the click happened on
  - what button / form / etc they clicked on
3. Your company buys advertisements on Facebook. To make business decisions on how you spend on ads, you'll want to make a table which has for each row:
  - the date
  - how much you spent
  - how many times the ads were viewed
  - how many times people clicked on the ads
  - how much revenue the ads generated

1. is raw data, that is 'small'. It could have erroneous information coming from site bugs, or people filling out forms incorrectly. There will probably be thousands of records for each day
2. is raw data, that is (probably) 'big'. There could be erroneous information, and there will probably be millions of records generated each day
3. is cleansed data, that is 'small'. Some analysts or engineers probably made this table, and spend time trying sure it doesn't contain any bogus information. There's only 1 record for each day, so the table is small.

## Gameplan

1. GUI overview
2. SELECT ... FROM ...
3. Comments and making your code readable
4. WHERE clause
5. (LEFT | RIGHT | OUTER | INNER) JOIN
6. CASE statements
7. GROUP BY
8. Aggregate functions: COUNT, SUM, COUNT(DISTINCT ), MIN, MAX
9. Sub queries
10. HAVING, ORDER BY, UNION [ALL]
11. CTEs (in most, but not all flavors of SQL)

## Resources

- I learned the basics from these tutorials: http://sqlzoo.net/
- People also like to learn from this: http://www.w3schools.com/sql/default.asp
- If you can't figure out how to do something or where your error is, google it.
  If you get good enough at reading your own errors, Google, and Stack Overflow you can solve almost all problems!
