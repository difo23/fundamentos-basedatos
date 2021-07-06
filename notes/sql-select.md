The [SQL](https://en.wikipedia.org/wiki/SQL) **SELECT** statement returns a [result set](https://en.wikipedia.org/wiki/Result_set) of records, from one or more [tables](https://en.wikipedia.org/wiki/Table_(database)).[[1\]](https://en.wikipedia.org/wiki/Select_(SQL)#cite_note-1)[[2\]](https://en.wikipedia.org/wiki/Select_(SQL)#cite_note-2)

A SELECT statement retrieves zero or more rows from one or more [database tables](https://en.wikipedia.org/wiki/Database_Tables) or database [views](https://en.wikipedia.org/wiki/View_(database)). In most applications, `SELECT` is the most commonly used [data manipulation language](https://en.wikipedia.org/wiki/Data_manipulation_language) (DML) command. As SQL is a [declarative programming](https://en.wikipedia.org/wiki/Declarative_programming) language, `SELECT` queries specify a result set, but do not specify how to calculate it. The database translates the query into a "[query plan](https://en.wikipedia.org/wiki/Query_plan)" which may vary between executions, database versions and database software. This functionality is called the "[query optimizer](https://en.wikipedia.org/wiki/Query_optimizer)" as it is responsible for finding the best possible execution plan for the query, within applicable constraints.

The SELECT statement has many optional clauses:

- `SELECT` clause is the list of columns or SQL expressions that must be returned by the query. This is approximately the [relational algebra](https://en.wikipedia.org/wiki/Relational_algebra) [projection](https://en.wikipedia.org/wiki/Projection_(relational_algebra)) operation.
- `AS` optionally provides an alias for each column or expression in the `SELECT` clause. This is the relational algebra [rename](https://en.wikipedia.org/wiki/Rename_(relational_algebra)) operation.
- `FROM` specifies from which table to get the data.[[3\]](https://en.wikipedia.org/wiki/Select_(SQL)#cite_note-3)
- `WHERE` specifies which rows to retrieve. This is approximately the relational algebra [selection](https://en.wikipedia.org/wiki/Selection_(relational_algebra)) operation.
- `GROUP BY` groups rows sharing a property so that an [aggregate function](https://en.wikipedia.org/wiki/Aggregate_function) can be applied to each group.
- `HAVING` selects among the groups defined by the GROUP BY clause.
- `ORDER BY` specifies how to order the returned rows.