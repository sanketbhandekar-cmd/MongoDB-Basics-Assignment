### Q1. MongoDB primarily stores application data as:
Q1: B (Documents)
- **Explanation:** MongoDB is a document-oriented NoSQL database that stores records as JSON-like BSON documents rather than relational rows, worksheets or files.

### Q2. Which field is automatically added and indexed by MongoDB to uniquely identify a document?
Q2: C (`_id`)
- **Explanation:** MongoDB automatically creates a unique `_id` field for every document (if not provided) and maintains a default index on it.

### Q3. Which option makes `updateOne()` insert a document when no matching document exists?
Q3: C (`{ upsert: true }`)
- **Explanation:** Enabling `{ upsert: true }` updates a matching document if one exists, or inserts a new document if none matches.

### Q4. Which operator adds a value to an array only if the value is not already present?
Q4: C (`$addToSet`)
- **Explanation:** Unlike `$push`, which always appends, `$addToSet` inserts an element only if it is not already in the array.

### Q5. Which aggregation stage is used to group documents?
Q5: B (`$group`)
- **Explanation:** The `$group` stage groups documents by a specified key (`_id`) so you can run accumulators like `$sum` and `$avg`.

### Q6. Which query correctly searches for employees whose address city is Pune?
Q6: C (`{ "address.city": "Pune" }`)
- **Explanation:** Nested document fields are queried using dot notation wrapped in quotes (`"address.city"`).

### Q7. Which approach stores related data directly inside the parent MongoDB document?
Q7: B (Embedding)
- **Explanation:** Embedding nests related data inside the same document, while referencing stores it in separate documents linked by an ID.

### Q8. What does the following command do? `db.employees.deleteMany({})`
Q8: C (Deletes all documents in the collection)
- **Explanation:** An empty filter `{}` matches every document in `employees` and deletes them, leaving the empty collection intact.

### Q9. Which is the recommended approach for application database credentials?
Q9: C (Store them using secure configuration/environment variables or secrets management)
- **Explanation:** Hard-coding or committing credentials exposes secrets; environment variables or secrets managers keep them secure.

### Q10. Which statement about MongoDB indexes is correct?
Q10: B (Only `_id` is automatically indexed by default.)
- **Explanation:** MongoDB only indexes `_id` automatically; other indexes should be created selectively for frequently queried or sorted fields.
