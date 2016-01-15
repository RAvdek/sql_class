# Joins

`JOIN` allows you to look up data in one table using a reference from another.

If you're good at Excel, think of this as equivalent to the `VLOOKUP` function.

... work though some examples ...

## Different types of joins

One trying to match one record from table A to another from table B, a few things can happen:
- There are one or more matches for the record in table A
- The record in table A has missing values
- The record in table A doesn't have missing values, but there is no match in table B

Different join types will specify the behavior you want in these cases:
- `select * from A JOIN B`: Only shows matches
- `select * from A LEFT JOIN B`: Will show every record in A, and only those of records of B having a match
- `select * from A RIGHT JOIN B`: Shows only the A records having a match, and every B record
- `select * from A OUTER JOIN B`: Every record shows up

This picture gives a sort-of-understandable summary
![http://www.codeproject.com/KB/database/Visual_SQL_Joins/Visual_SQL_JOINS_orig.jpg]
