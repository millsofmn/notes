# SQL

SQL is set-oriented because it operates over the entire table not row-by-row.

## Vocabulary

* **Base Table** is the table on which a view is based.
* **Batch Update Routine** a routine that pools transactions into a single group 
to update the master table in a single operation.
* **Cross Join** is the cartesian product of two tables.
* **Outer Join** returns not only the rows matching the join condition but also
the rows with unmatched values.
  * **FULL OUTER JOIN** - include everything from the left and right tables.
  * **LEFT [OUTER] JOIN** - include everything in the left table
  * **RIGHT [OUTER] JOIN** - include everything in the right table
  * **FULL [OUTER] JOIN** - inlcude everything in both tables
* **INNER JOIN** only rows that match the given criteria are returned.
* **Subquery** is a query located in another query and can return:
  1. a single value (one row, one column)
  1. a list of values  (many rows, one column)
  1. a virtual table (many rows, many columns)
* **Correlated Query** is a query that will execute once for each row in the outer 
query (like a nested loop) usually can be found in the where clause.
* **Relation Set Operators** will join one result set with another. The relation 
must have identical names and compatible data types. 
  * **UNION** joins result sets together _without_ duplicates.
  * **UNION ALL** joins result sets toghter _with_ duplicates.
  * **INTERSECT** the result set will return only what is in both sets.
  * **MINUS** the result set will include everything in the first set not found in the second set.
* **OPERATORS**
  * **ALL** operator allow you to compare a single value with a list of values returned by a subquery.
  
## Join Examples

### USING

    SELECT column-list
    FROM table1 JOIN table2 USING(column)
    
### NATURAL

Join tables based on common columns so there need to be some identical column name and types to join on.

    SELECT column-list
    FROM table1 NATURAL JOIN table1
