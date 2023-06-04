
# Relational Databases

<div v-click>
In a relational database, data is stored in multiple related tables, and the relationships between these tables are defined through keys. The primary key uniquely identifies each row in a table, while foreign keys establish relationships between tables by referring to the primary keys of other tables.
</div>

<div v-click="2" style="margin-top: 16px">
Relational databases use SQL as the standard language for defining, manipulating, and querying the data. SQL allows users to perform operations like inserting, updating, and deleting data, as well as retrieving specific subsets of data using queries.
</div>


---


# Key features


<div v-click>
- Data Integrity: Relational databases enforce integrity constraints to ensure data consistency and accuracy. These constraints include primary key uniqueness, foreign key references, and data type validation.
</div>
<div v-click="2" style="margin-top: 16px">
- ACID Compliance: Relational databases adhere to ACID (Atomicity, Consistency, Isolation, Durability) properties, which guarantee transactional consistency and reliability.
</div>
<div v-click="3" style="margin-top: 16px">
- Ad hoc Queries: Relational databases provide flexibility in querying data using SQL. Users can write ad hoc queries to retrieve specific information based on their requirements.
</div>

<div v-click="4" style="margin-top: 16px">
- Scalability: Relational databases can handle large volumes of data and are designed to scale horizontally by distributing data across multiple servers or vertically by adding more resources to a single server.
</div>


---

# Add new element to relational database

The time complexity of inserting data into a database can vary depending on several factors, including the database system being used, the table structure, the indexing strategy, and the volume of data being inserted. 

Inserting a single row into a table typically has a time complexity of O(1) or constant time. The database engine performs necessary validations, checks constraints, and writes the data to the appropriate location in the database.

Additionally, the time complexity of an insert operation may be influenced by other factors, such as the presence of triggers, indexes, constraints, and concurrent operations on the database.

--- 

# Search element

--- 

# Delete element


--- 

# Indexing

<div v-click>

## B-Tree Index

- Searching: O(log n), where n is the number of entries in the index.
- Insertion: O(log n), as the B-tree needs to be rebalanced if necessary.
- Deletion: O(log n), as the B-tree needs to be rebalanced if necessary.

</div>


<div v-click="2" style="margin-top: 16px">

## Hash Index:

- Searching: O(1) on average, assuming a well-distributed hash function.
- Insertion: O(1) on average, assuming no collisions occur.
- Deletion: O(1) on average, assuming no collisions occur.

</div>

---

# Indexing (cont.)

<div v-click>

## Bitmap Index:
- Searching: O(1), as bitmap indexes provide direct bit-level access.
- Insertion: O(n), as updating the bitmap can involve scanning and modifying multiple bits.
- Deletion: O(n), as updating the bitmap may require scanning and modifying multiple bits.

</div>

<div v-click="2" style="margin-top: 16px">

## Sparse Index:

- Searching: O(log n), where n is the number of entries in the index.
- Insertion: O(1) or O(log n), depending on the specific implementation and insertion strategy.
- Deletion: O(1) or O(log n), depending on the specific implementation and deletion strategy.

</div>

