```
Return ALL the data in the 'movies' table.
SELECT * FROM movies
```
```
Return ONLY the name column from the 'people' table
SELECT name FROM people
```
```
Oops! Someone spelled Krusty The Clown's name wrong! Change it to reflect the
proper spelling (Crusty should be Krusty).
UPDATE people
SET name = 'Krusty the Clown'
WHERE name = 'Crusty the Clown'
```
```
Return ONLY Homer Simpson's name from the 'people' table.
SELECT name FROM people
WHERE name = 'Homer Simpson'
```
```
The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.
DELETE FROM movies
WHERE title = 'Batman Begins'
```
```
We forgot one of the main characters! Add Bart Simpson to the 'people' table
INSERT INTO people (name)
VALUES ('Bart Simpson')
```
```
Eric Cartman has decided to hijack our movie evening, Remove him from the table of people.
DELETE FROM people
WHERE name = 'Eric Cartman'
```
```
The cinema has just heard that they will be holding an exclusive midnight showing of 'Avengers: Infinity War'!! Create a new entry in the 'movies' table to reflect this.
INSERT INTO movies (title)
VALUES ('Avengers: Infinity War')
```
```
The cinema would like to make the Iron Man movies a triple billing. Find out the show time of "Iron Man 2" and set the show time of "Iron Man 3" to start two hours later.

SELECT show_time FROM movies
WHERE title = 'Iron Man 2'
[returns show_time of 18.45]

UPDATE movies
SET show_time = '20.45'
WHERE title = 'Iron Man 3'
```

```
<<EXTENSION>>

To delete one row from a table
DELETE FROM <table_name>
WHERE row_id number = <value>

To delete all rows in a table
 DELETE FROM <table_name>

To delete rows in multiple tables (two methods)
  execute two DELETE statements
    DELETE FROM table
    WHERE <value> = <value to be deleted>
      and
    DELETE FROM other table
    WHERE <value> = <value to be deleted>

    <<OR>>

    Create a foreign key constraint so that if you delete a row in a table, the corresponding rows the related table are also removed automatically.

    In case the database management system does not support the foreign key constraint, you have to execute both DELETE statements in a single transaction to make sure that the statements execute in all-or-nothing mode.




```
