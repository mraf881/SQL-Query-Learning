# This is the place where I store used query in Google BigQuery for future references.

**Query001**

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

`SELECT DISTINCT * FROM dataset.table` --Selecting Unique rows from the dataset.

**Query003**

`SELECT *, Column_ID as Column_New FROM dataset.table` --Selecting all column and renaming column to desired name from the dataset but it only add new column at the end of table.

Output:
|Column_ID|Column2|Column3|Column_New|
|-------|-------|-------|--|
|1|test|test|1
|2|test|test|2
|\*|\*|\*|\*|
|\*\*|\*\*|\*\*|\*\*|
|\*\*\*|\*\*\*|\*\*\*|\*\*\*|

**Query004**

`SELECT * EXCEPT(Column_ID), Column_ID as Column_New FROM dataset.table` --Using EXCEPT() to not include renamed column.

Output:
|Column2|Column3|Column_New|
|-------|-------|--|
|test|test|1
|test|test|2
|\*|\*|\*|
|\*\*|\*\*|\*\*|
|\*\*\*|\*\*\*|\*\*\*|


**Query004**

`SELECT * FROM dataset.table WHERE COLUMN3 IS NULL` --Selecting the column1 contain null value.

Output:
|Column_1|Column2|Column3|
|-------|-------|-------|
|4|test|null|
|5|test|null|
|\*\*\*|\*\*\*|\*\*\*|


**QUERY005**

`SELECT * FROM dataset.table ORDER BY Column1 DESC LIMIT 3` --To show the result in descending order.

|Column_ID|Column2|Column3|
|-------|-------|-------|
|3|test|test|
|2|test|test|
|1|test|test|
