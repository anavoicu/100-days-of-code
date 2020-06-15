# 100 Days Of Code - Log

### Day 0: Sunday, 07.06.2020


**Today's Progress**: I am getting organized for starting the 100-days-of-code challenge.

**Thoughts:** I can hardly wait to start and I am really excited to finishing this challenge successfully.


### Day 1: Monday, 08.06.2020

**Today's Progress**: I started reading "The Definitive Guide to DAX", by Marco Russo and Alberto Ferrari. The first chapter ("What is DAX?") contains an introduction about the DAX language and its usage. 


### Day 2: Tuesday, 09.06.2020

**Today's Progress**: I started Chapter 2 ("Introducing DAX"). This one contains more information about the language and it's a really great starting point for learning DAX. You get the chance to understand the difference between a calculated column and a calculated measure and how to choose which one you need in your calculations. I learned how to use variables in my calculations and how to format DAX code.


### Day 3: Wednesday, 10.06.2020

**Today's Progress**: I still had some pages from Chapter 2, which I've read today. I learned about the aggregated functions in DAX, like `MIN()`, `MAX()`, `SUM()`, `AVERAGE()`, `STDEV()`. These functions receive a column as parameter. If you need to use apply an aggregation function on an expression (instead of a single column), you need to use an iterator. 

 An iterator is a function that receives two parameters:

- the table that is scanned
- the expression which will be evaluated to every row of the table.

Most aggregated functions have a corresponding iterator: 
`AVERAGE() -> AVERAGEX()`
`SUM() -> SUMX()`
`MIN() -> MINX()`
`MAX() -> MAXX()`

Summary: 
1. The aggregated functions are actually iterators hidden behind an easier syntax.
2. There is no difference in performance between using an aggregated function and an iterator.

**Thoughts:** I feel that I am not making as much progress as I would like. This is a bit demotivating and I keep telling myself that nobody is rushing me and every little thing I'm doing in this challenge is better than nothing. 


### Day 4: Thursday, 11.06.2020

**Today's Progress**: Today I played with:
1. Logical functions: `AND()`, `OR()`, `NOT()`, `TRUE()`, `FALSE()`, `IF()`. 
`SWITCH()` is also really useful in DAX and I'm glad it exists. It is a lot easier to read and understand than writing nested `IF` functions.

2. Information functions: `ISBLANK()`, `ISERROR()`, `ISNUMBER()`, `ISTEXT()`
I am not sure how useful is `ISERROR()` when writing DAX formulas. 

3. Math functions:  `ABS()`, `POWER()`, `SQRT()`, `SIGN()`, `FLOOR()`, `CEILING()`, `ROUND()`.

4. Text functions: `CONCATENATE()`, `CONCATENATEX()`, `FORMAT()`, `LEN()`.

5. Relational functions: `RELATED()`, `RELATEDTABLE()`
- `RELATED()` is used to access the one-side of a one-to-many relationship, so only one row is returned.
- `RELATEDTABLE()` accesses the many-side of a one-to-many relationship and it returns a table with the related rows.

*Important to remember:* These functions can follow a chain of relationships and retrieve the needed result. They always start from the one-side and move towards the many-side.

**Thoughts:** There are so many functions and I'm not even creating examples for all of them. My progress is slow and this makes me a bit anxious.


### Day 5: Friday, 12.06.2020

**Today's Progress**: I'm starting Chapter 3 today ("Using basic table functions"). I learned about: 
1. `EVALUATE()`
2. I played around with DAX Studio. My Dax Studio is currently in Dutch and I don't know how to change it :)
3. `FILTER(table, condition)`. 
- This is a function that selects from the given table only the rows that satisfy the condition. 
- You can also use nested FILTERs. However, you need to make sure that performance is not greatly affected when you do that. 
- If one condition is more selective, apply it first when using the nested FILTER.


### Day 6: Saturday, 13.06.2020

**Today's Progress**: Learned about the following:
1. `ALL()`

- Returns all the rows of a table or all the values of one or more columns, depending on the parameters used.
- It ignores all the filters introduced in the report
- It's useful for calculating ratios or percentages.

2. `ALLEXCEPT()`

- Similar to `ALL()`
- Receives as parameters: the table needed and a list of columns to be excluded from the end-result.

3. `VALUES()`

- Returns the distinct values from a column, taking into account the filters in the current report.
- If the blank row is present in the table, it returns it.

4. `DISTINCT()`

- Returns the distinct values from a column, taking into account the filters in the current report, but does not return the blank row.
- If the model is correct, (there are no invalid relationships), `DISTINCT()` and `VALUES()` have the same behaviour. 

5. `ALLSELECTED()`

- Retrieves the list of values of a table (or a column) as visible in the current report. 
- It takes into consideration all (and only!) the filters outside of the current report
- *Important:* It is the most complex table function and sometimes, it produces unexpected results (because people don't really understand its behavior, not that it's something wrong with it).


### Day 7: Sunday, 14.06.2020

**Today's Progress**: I read again Chapter 3 and looked through the examples. 

**Thoughts:** Somehow, things don't look that bad anymore.


### Day 8: Monday, 15.06.2020

**Today's Progress**: I started with Chapter 4 ("Understanding evaluation contexts"). I know it is a very important chapter so I'm reading everything extra carefully, but it doesn't seem that bad so far.

**Thoughts:** 

**Link to work:**