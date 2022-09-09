# This is the place where I store used query in Google BigQuery for future references.
- Feel free to comment.

**Query001**

Query: 

`SELECT * FROM dataset.table LIMIT 1000` --Selecting all column from all column and limit 1000 result.

Output:
|Column1|Column2|Column3|
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
