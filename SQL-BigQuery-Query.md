# This is the place where I store used query in Google BigQuery for future references.
- Feel free to comment.
- Give positive feedback.
- FYI, this is markdown file.
- Some of the queries, I do not include output. Sorry about that.

**Query001**

Query: 

`SELECT * FROM dataset.table LIMIT 1000` --Selecting all column from all column and limit 1000 result.

Output:
|Column_ID|Column2|Column3|
|-------|-------|-------|
|1|test|test|
|2|test|test|
|\*|\*|\*|
|\*\*|\*\*|\*\*|
|\*\*\*|\*\*\*|\*\*\*|
|1000|test|test|

**Query002**

Query:

`SELECT DISTINCT * FROM dataset.table` --Selecting Unique rows from the dataset.

**Query003**

Query:

`SELECT *, Column_ID as Column_New FROM dataset.table` --Selecting all column and renaming column to desired name from the dataset but it only add new column at the end of table.

Output:
|Column_ID|Column2|Column3|Column_One|
|-------|-------|-------|--|
|1|test|test|1
|2|test|test|2
|\*|\*|\*|\*|
|\*\*|\*\*|\*\*|\*\*|
|\*\*\*|\*\*\*|\*\*\*|\*\*\*|

**Query004**

Query:

`SELECT * EXCEPT(Column_ID), Column_ID as Column_New FROM dataset.table` --Using EXCEPT() to not include renamed column.

Output:
|Column2|Column3|Column_One|
|-------|-------|--|
|test|test|1
|test|test|2
|\*|\*|\*|
|\*\*|\*\*|\*\*|
|\*\*\*|\*\*\*|\*\*\*|

