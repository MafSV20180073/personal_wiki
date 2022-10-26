# SQL Indexes Best Practices

***

## How to get the most out of your indexes:

1. Use statement plans to see how your database services your query;
2. Filter your query with your index to avoid a full table scan;
3. Sort your query with your index to speed up the query;
4. Cover your query with your index to avoid the table entirely.

***

A good index will:

- Filter the data efficiently;
- Eliminate the need to sort the data;
- Answer your query with data found in the index.

### Using statement plans to see how the database services the query

- Add a visibility command to your query so you can understand what the database is doing at each stage when running the query (and identify the pain-points of your query). Example:

```
EXPLAIN ANALYZE SELECT title, body, datetime
                FROM messages
                WHERE email = 'person@example.com'
                ORDER BY datetime DESC
                LIMIT 10;
```

### Filter your query with your index

- This aims to avoid a full table scan;
- The only way to avoid scanning the entire table is to build an index.

### Sort your query with your index

- This aims to speed up the query;
- A better index should include information on the timestamp;
- Index can be composed by more than 1 column.

### Cover your query with your index

- This aims to avoid the table entirely;
- In other words, if possible, the information you need should be covered by the index itself.

<br>

## Caveats to these index best practices:

- Indexes have to be kept in synch with the table rows they point to (i.e., you will need a transaction when writing to a row, so try to not build too many indexes on a table);
- If you index a large field, you'll have a large index (try to avoid that);
- Always use a visibility command to check if things are working properly and the way you're expecting.

<br>

<br>

<b>Main sources:</b>
- https://www.cockroachlabs.com/blog/sql-performance-best-practices/
