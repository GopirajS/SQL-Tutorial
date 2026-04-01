<a href="#top" id="backToTop" style="
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: #007bff;
    color: white;
    padding: 8px 12px;
    border-radius: 6px;
    text-decoration: none;
    font-size: 14px;
">⬆ Top</a>

<script>
document.querySelector('#backToTop').addEventListener('click', function(e) {
    e.preventDefault();
    document.querySelector('#top').scrollIntoView({
        behavior: 'smooth'
    });
});
</script>

<h1 style="text-align:center;" >Sql Learning – Complete Question Bank</h1>

## Basics

* [What is SQL and why is it used?](#What_is_SQL_and_why_is_it_used)
* [What are the differences between SQL, MySQL, PostgreSQL, and SQLite?](#D_between_SQL_MySQL_PostgreSQL_and_SQLite)
* What is a database?
* What is a table, row, and column?
* [What is a primary key ,foreign key and Unique Key?](#primary_foreign_Unique_Key)
* [What are NULL values?](#What_is_a_NULL_value)
* [What is the difference between DELETE, TRUNCATE, and DROP?](#DB_DELETE_TRUNCATE_and_DROP)
* [What is a schema?](#What_is_a_Schema)
* [What are data types in SQL?](#What_are_Data_Types_in_SQL)

---

## Data Definition Language (DDL)

* [What is DDL?](#What_is_DDL)
* [What are constraints?](#What_are_Constraints)
* [What is NOT NULL constraint?](#What_is_NOT_NULL_Constraint)
* [What is UNIQUE constraint?](#What_is_UNIQUE_Constraint)
* [What is CHECK constraint?](#What_is_CHECK_Constraint)
* [What is DEFAULT constraint?](#What_is_DEFAULT_Constraint)


## Data Manipulation Language (DML)

* [What is DML?](#What_is_DML)
* [What is the difference between INSERT and INSERT IGNORE?](#INSERT_and_INSERT_IGNORE)
* [What is UPSERT?](#What_is_UPSERT)
* [What is LIMIT and OFFSET?](#What_is_LIMIT)
* [What is ORDER BY?](#What_is_ORDER_BY)
* [What is DISTINCT?](#What_is_DISTINCT)
* [What is alias (AS)?](#What_is_Alias)



## Filtering and Conditions

* What is the WHERE clause?
* What are comparison operators?
* What is BETWEEN?
* What is IN?
* What is LIKE?
* What is the difference between LIKE and REGEXP?
* What is "IS NULL" vs "= NULL"?
* What are logical operators (AND, OR, NOT)?

## Aggregate Functions

* [What are aggregate functions?](#What_are_Aggregate_Functions)
* Use of COUNT, SUM, AVG, MAX, MIN
* [What is GROUP BY?](#What_is_GROUP_BY)
* [What is HAVING?](#What_is_HAVING)
* [Difference between WHERE and HAVING?](#WHERE_vs_HAVING)


## Joins

* [What is a JOIN?](#What_is_a_JOIN)
* [What is INNER JOIN(JOIN)?](#What_is_INNER_JOIN)
* [What is LEFT JOIN?](#What_is_LEFT_JOIN)
* [What is RIGHT JOIN?](#What_is_RIGHT_JOIN)
* [What is FULL OUTER JOIN?](#What_is_FULL_OUTER_JOIN)
* [What is CROSS JOIN?](#What_is_CROSS_JOIN)
* [What is SELF JOIN?](#What_is_SELF_JOIN)
* [Difference between JOIN and SUBQUERY?](#Difference_between_JOIN_and_SUBQUERY)
* How do joins impact performance?

## Subqueries

* [What is a subquery?](#What_is_a_Subquery)
* [Types of Subqueries in SQL?](#Types_of_Subqueries_in_SQL) 
* Subquery vs JOIN – when to use which?
* What is EXISTS?
* What is NOT EXISTS?


## Set Operations

* [What is UNION?](#What_is_UNION)
* [What is UNION ALL?](#What_is_UNION_ALL)
* [What is INTERSECT?](#What_is_INTERSECT)
* [What is EXCEPT / MINUS](#What_is_EXCEPT_MINUS)

## String Functions

* What is CONCAT()?
* What is LENGTH()?
* What is SUBSTRING()?
* What is TRIM()?
* What is REPLACE()?
* What is LOWER() and UPPER()?

## Date & Time Functions

* What are date data types?
* What is NOW()?
* What is CURDATE()?
* How to calculate date differences?
* How to extract year/month/day from a date?
* How to filter records by date range?


## Indexes

* [What is an index?](#What_is_an_Index)
* [Types of indexes?](#Types_of_Indexes_in_SQL)
* Why are indexes used?
* What is a composite index?
* When should you avoid indexes?
* What is index selectivity?

## Views

* What is a view?
* View vs Table?
* Why use views?
* How to create a view?
* Can views be updated?

## Transactions

* [What is a transaction?](#What_is_a_Transaction)
* [What is COMMIT?](#What_is_COMMIT)
* [What is ROLLBACK?](#What_is_ROLLBACK)
* [What is SAVEPOINT?](#What_is_SAVEPOINT)
* [What are ACID properties?](#What_are_ACID_Properties)


## Stored Procedures & Functions

* What is a stored procedure?
* Stored procedure vs function?
* How to create a stored procedure?
* What are parameters?
* What is control flow in SQL (IF, CASE, LOOP)?

## Locks & Concurrency

* What is database locking?
* What is row-level locking?
* What is table-level locking?
* What is a deadlock?
* How to prevent deadlocks?

## Normalization & Design

* What is database normalization?
* What is 1NF?
* What is 2NF?
* What is 3NF?
* What is denormalization?
* When should denormalization be used?

## Performance & Optimization

* How do you optimize SQL queries?
* What is query execution plan?
* What is EXPLAIN?
* How to find slow queries?
* Index vs Query optimization?

## Security

* What is SQL Injection?
* How to prevent SQL Injection?
* What is prepared statement?
* What are database user roles?
* What are GRANT and REVOKE?

## Advanced SQL

* What are window functions?
* What is ROW_NUMBER()?
* What is RANK() and DENSE_RANK()?
* What is PARTITION BY?
* What is CTE (WITH clause)?
* Recursive CTE – what and why?

## Practical & Scenario-Based

* Write a query to find duplicate records
* Write a query to get the second highest salary
* Find employees without managers
* Get top N records per group
* Delete duplicate rows safely
* Paginate results using SQL
* Design a database for an e-commerce system




<hr style="border: 2px solid green;">

<h1 style="text-align:center;" >SQL Basics</h1>

![Image](https://github.com/user-attachments/assets/6c1a0e04-7bc4-4fd1-8917-a3195089cd3d)

<h2 id="What_is_SQL_and_why_is_it_used" style="color:green; text-align:center;">What is SQL and why is it used?</h2>

**🗄️ What is SQL?**
SQL stands for **Structured Query Language**.

**💬 What does it do?**
SQL is used to **communicate with a database**.

**🎯 Why is SQL used?**

* 📥 **Get data** from the database
* ➕ **Insert new data**
* ✏️ **Update existing data**
* 🗑️ **Delete data**
* 🧱 **Create and manage tables**

**🧠 Simple example:**
If a database is a **cupboard 🗄️**,
SQL is the **language 🗣️** you use to ask for or store files 📁.

If you want, I can continue **all SQL topics with icons** step-by-step 👍



<hr style="border: 2px solid green;">

<h2 id="D_between_SQL_MySQL_PostgreSQL_and_SQLite" style="color:green; text-align:center;">What are the differences between SQL, MySQL, PostgreSQL, and SQLite?</h2>


### 🧠 SQL vs Databases (Easy Way)

#### 📘 **SQL**

* 🗣️ **Language**, not a database
* 📜 Used to **write queries**
* 🧠 Works with many databases

👉 Example: `SELECT * FROM users;`

---

### 🐬 **MySQL**

* 🗄️ **Database software**
* ⚡ Fast and popular for **web apps**
* 🌐 Common with **PHP / Laravel**
* 🆓 Open-source

👉 Uses **SQL language**

---

### 🐘 **PostgreSQL**

* 🗄️ **Database software**
* 🧠 Very **powerful & advanced**
* 🔐 Strong in **security & data integrity**
* 📊 Best for **complex queries & large systems**

👉 Uses **SQL language**

---

### 📦 **SQLite**

* 🗄️ **Lightweight database**
* 📁 Stored as a **single file**
* 🚀 No server needed
* 📱 Common in **mobile & small apps**

👉 Uses **SQL language**

---

### ⚖️ Quick Comparison Table

| 🔍 Feature    | SQL      | MySQL    | PostgreSQL    | SQLite      |
| ------------- | -------- | -------- | ------------- | ----------- |
| Type          | Language | Database | Database      | Database    |
| Server Needed | ❌        | ✅        | ✅             | ❌           |
| Best For      | Queries  | Web apps | Enterprise    | Small apps  |
| Performance   | —        | Fast     | Very powerful | Lightweight |

---

### 🧠 Simple Analogy

* 🗣️ **SQL** → Language you speak
* 🐬 **MySQL / 🐘 PostgreSQL / 📦 SQLite** → Different **people** who understand SQL


<hr style="border: 2px solid green;">

<h2 id="primary_foreign_Unique_Key" style="color:green; text-align:center;">What is a primary key ,foreign key and Unique Key</h2>

### 🔑 **Primary Key**

* 🆔 **Uniquely identifies** each row in a table
* 🚫 **Cannot be NULL**
* 🔁 **No duplicate values**
* 📌 Only **one primary key** per table

👉 Example:

```sql
id INT PRIMARY KEY
```

🧠 Think of it as: **Aadhar / Passport number** – one per person

---

### 🔗 **Foreign Key**

* 🤝 Creates a **relationship between tables**
* 🔁 Refers to a **Primary Key in another table**
* 🚫 Prevents invalid data
* 📌 Can have **duplicate values**

👉 Example:

```sql
user_id INT REFERENCES users(id)
```

🧠 Think of it as: **Employee belongs to a department**

---

### ⭐ **Unique Key**

* 🆔 Ensures **unique values**
* ✅ Allows **NULL values** (usually)
* 📌 A table can have **multiple unique keys**

👉 Example:

```sql
email VARCHAR(255) UNIQUE
```

🧠 Think of it as: **Email ID** – unique but optional

---

### ⚖️ Quick Comparison Table

| Feature       | 🔑 Primary Key | 🔗 Foreign Key | ⭐ Unique Key |
| ------------- | -------------- | -------------- | ------------ |
| Unique Values | ✅              | ❌              | ✅            |
| Allows NULL   | ❌              | ✅              | ✅            |
| Duplicates    | ❌              | ✅              | ❌            |
| Per Table     | One            | Many           | Many         |
| Purpose       | Identity       | Relationship   | Uniqueness   |

---

### 🧠 Simple Summary

* 🔑 **Primary Key** → Who you are
* 🔗 **Foreign Key** → Who you belong to
* ⭐ **Unique Key** → Special identity (like email)


<hr style="border: 2px solid green;">

<h2 id="What_is_a_NULL_value" style="color:green; text-align:center;">What is a NULL value?</h2>


### ❓ **What is a NULL value?**

* **NULL** means **no value**
* It is **not 0**, **not empty**, and **not false**
* It means **data is unknown or missing**

---

### 🧠 Easy Examples

* 👤 User has **no phone number yet** → `NULL`
* 📅 End date **not decided** → `NULL`
* 📍 Address **not provided** → `NULL`

---

### ⚠️ Important Points

* 🚫 `NULL ≠ 0`
* 🚫 `NULL ≠ ''` (empty string)
* 🚫 `NULL ≠ FALSE`

---

### 🧪 How to check NULL

* ❌ Wrong:

```sql
WHERE phone = NULL
```

* ✅ Correct:

```sql
WHERE phone IS NULL
WHERE phone IS NOT NULL
```

---

### ⚖️ NULL vs Empty vs Zero

| Type   | Meaning     |
| ------ | ----------- |
| `NULL` | No value    |
| `''`   | Empty text  |
| `0`    | Number zero |

---

### 🧠 Simple Analogy

* 📦 **NULL** = Box is **missing**
* 📭 **Empty string** = Box is there but empty
* 🔢 **0** = Box has value zero

---

### 🔑 Why NULL matters

* Helps represent **unknown or optional data**
* Prevents **wrong assumptions**
* Important for **conditions & calculations**


<hr style="border: 2px solid green;">

<h2 id="DB_DELETE_TRUNCATE_and_DROP" style="color:green; text-align:center;">What is the difference between DELETE, TRUNCATE, and DROP?</h2>


### 🗑️ **DELETE**

* ❌ Removes **selected rows**
* 🎯 Can use **WHERE condition**
* 🔄 Can be **rolled back** (with transaction)
* 🧱 Table structure **stays**

👉 Example:

```sql
DELETE FROM users WHERE id = 5;
```

🧠 Use when: you want to delete **specific data**

---

### 🚿 **TRUNCATE**

* ❌ Removes **all rows**
* ⚡ Very **fast**
* 🚫 **Cannot use WHERE**
* 🔄 Usually **cannot be rolled back**
* 🧱 Table structure **stays**
* 🔢 Resets **AUTO_INCREMENT**

👉 Example:

```sql
TRUNCATE TABLE users;
```

🧠 Use when: you want to **empty the table**

---

### 💣 **DROP**

* ❌ Removes **entire table**
* 🏗️ Table structure **deleted**
* 🚫 Data + table = **gone forever**
* 🔄 Cannot be rolled back

👉 Example:

```sql
DROP TABLE users;
```

🧠 Use when: you **don’t need the table anymore**

---

### ⚖️ Quick Comparison Table

| Feature       | 🗑️ DELETE | 🚿 TRUNCATE | 💣 DROP |
| ------------- | ---------- | ----------- | ------- |
| Deletes Rows  | Some / All | All         | All     |
| WHERE Allowed | ✅          | ❌           | ❌       |
| Rollback      | ✅          | ❌           | ❌       |
| Table Exists  | ✅          | ✅           | ❌       |
| Speed         | Slow       | Fast        | Fastest |

---

### 🧠 Simple Analogy

* 🗑️ **DELETE** → Remove some files
* 🚿 **TRUNCATE** → Empty the folder
* 💣 **DROP** → Delete the folder itself



<hr style="border: 2px solid green;">

<h2 id="What_)is_)a_)Schema" style="color:green; text-align:center;">What is a Schema?</h2>

### 🗂️ **What is a Schema?**

* A **schema** is a **logical container** inside a database
* It helps **organize database objects**
* Acts like a **folder** for tables, views, functions, etc.

---

### 🧠 Easy Example

* 🗄️ **Database** → Big cupboard
* 📁 **Schema** → Folder inside the cupboard
* 📄 **Table** → Files inside the folder

👉 Example:

```sql
sales.orders
```

`sales` = schema
`orders` = table

---

### 🎯 Why Schemas are useful

* 🧹 Better **organization**
* 🚫 Avoid **name conflicts**
* 🔐 Control **access & permissions**
* 🧠 Improves **clarity in large systems**

---

### 📌 Important Points

* A database can have **multiple schemas**
* Same table name can exist in **different schemas**
* Default schema is often **public** (PostgreSQL) or **dbo** (SQL Server)

---

### 🧠 Simple Analogy

* 🏢 **Building** = Database
* 🗂️ **Rooms** = Schemas
* 🪑 **Items** = Tables

---

### 📘 Example Use Case

* `auth.users`
* `sales.orders`
* `inventory.products`

### Interview Ans:

* 🗂️ **Schema:**
  *A schema is a logical container that organizes database objects like tables and views within a database.*


<hr style="border: 2px solid green;">

<h2 id="What_are_Data_Types_in_SQL" style="color:green; text-align:center;">🧾 What are Data Types in SQL?</h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/d78661b5-d972-4e18-9cba-ca580f2950d6" />


* Data types define **what kind of data** a column can store
* They control **storage, format, and valid values**


### 📦 SQL Data Types (All Types)

### 🔢 **Numeric Data Types**

* `INT` / `INTEGER` → Whole numbers
* `SMALLINT` → Small numbers
* `BIGINT` → Very large numbers
* `DECIMAL(p,s)` / `NUMERIC` → Exact values (money)
* `FLOAT` / `REAL` / `DOUBLE` → Decimal numbers

---

### 🔤 **String / Character Data Types**

* `CHAR(n)` → Fixed-length text
* `VARCHAR(n)` → Variable-length text
* `TEXT` → Long text

---

### 📅 **Date & Time Data Types**

* `DATE` → Date only
* `TIME` → Time only
* `DATETIME` → Date & time
* `TIMESTAMP` → Date & time (with timezone support in some DBs)
* `YEAR` → Year only

---

### 🔘 **Boolean Data Type**

* `BOOLEAN` / `BOOL` → True / False

---

### 📦 **Binary Data Types**

* `BINARY` → Fixed binary data
* `VARBINARY` → Variable binary data
* `BLOB` → Images, files, media

---

### 🧩 **Special / Advanced Data Types**

* `ENUM` → One value from a list
* `SET` → Multiple values from a list
* `JSON` → JSON formatted data
* `UUID` → Unique identifier
* `XML` → XML data

---

### 🌍 **Database-Specific Types**

* 🐘 PostgreSQL → `ARRAY`, `HSTORE`, `INET`, `JSONB`
* 🐬 MySQL → `GEOMETRY`, `POINT`
* 🪟 SQL Server → `MONEY`, `UNIQUEIDENTIFIER`

---

## 🎯 One-Line Interview Answer

* **Data Types:**
  *SQL data types define the kind of data a column can store, such as numbers, text, dates, or binary data.*

---

### 🧠 Memory Tip

* 🔢 Number
* 🔤 Text
* 📅 Date/Time
* 🔘 Boolean
* 📦 Binary
* 🧩 Special


<hr style="border: 2px solid green;">


<h1 style="text-align:center;" >Data Definition Language (DDL)</h1>

<h2 id="What_is_DDL" style="color:green; text-align:center;">  🏗️ What is DDL? </h2>

* **DDL** stands for **Data Definition Language**
* Used to **define, create, modify, and delete database structure**
* It works on **tables, schemas, indexes, and databases**

---

### 🧰 Common DDL Commands

* 🧱 `CREATE` → Create table/database
* ✏️ `ALTER` → Modify table structure
* 🗑️ `DROP` → Delete table/database
* 🚿 `TRUNCATE` → Remove all rows from a table

---

### 🧠 Simple Example
Below are **simple, clear examples** for **all common DDL queries** 😊
(Interview-ready + beginner friendly)

---

### 🧱 CREATE DATABASE

```sql
CREATE DATABASE school;
```

👉 Creates a new database named **school**

---

### 🗄️ CREATE TABLE

```sql
CREATE TABLE students (
  id INT PRIMARY KEY,
  name VARCHAR(50),
  age INT
);
```

👉 Creates a **students** table

---

### ✏️ ALTER TABLE (Add Column)

```sql
ALTER TABLE students
ADD email VARCHAR(100);
```

👉 Adds a new column **email**

---

### ✏️ ALTER TABLE (Modify Column)

```sql
ALTER TABLE students
MODIFY age SMALLINT;
```

👉 Changes column data type

---

### 🗑️ DROP TABLE

```sql
DROP TABLE students;
```

👉 Deletes the table completely

---

### 🚿 TRUNCATE TABLE

```sql
TRUNCATE TABLE students;
```

👉 Deletes all rows, keeps structure

---

### 🏷️ CREATE INDEX

```sql
CREATE INDEX idx_name
ON students(name);
```

👉 Improves search speed on **name**

---

### 🏷️ CREATE UNIQUE INDEX

```sql
CREATE UNIQUE INDEX idx_email
ON students(email);
```

👉 Ensures **email is unique**

---

### ❌ DROP INDEX

```sql
DROP INDEX idx_name;
```

👉 Removes the index

---

### 🧠 One-Line Interview Summary

* **CREATE** → Makes database/table
* **ALTER** → Changes structure
* **DROP** → Deletes structure
* **TRUNCATE** → Clears data
* **INDEX** → Speeds up search

---

### 📌 Memory Trick

🏗️ Build → ✏️ Change → 🚿 Clean → 💣 Remove → ⚡ Speed

---

### 🎯 One-Line Interview Answer

* **DDL:**
  *DDL is a set of SQL commands used to define and manage the structure of database objects.*


<hr style="border: 2px solid green;">

<h2 id="What_are_Constraints" style="color:green; text-align:center;">  ⛓️ What are Constraints? </h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/162df1cf-960d-45cb-a78a-177bcc0e6703" />

* Constraints are **rules applied to table columns**
* They **control what data is allowed**
* Help maintain **data accuracy and integrity**

---

### 📌 Common SQL Constraints (with examples)

#### 🔑 **PRIMARY KEY**

```sql
id INT PRIMARY KEY
```

👉 Unique + Not NULL

---

#### ⭐ **UNIQUE**

```sql
email VARCHAR(100) UNIQUE
```

👉 No duplicate values

---

#### 🚫 **NOT NULL**

```sql
name VARCHAR(50) NOT NULL
```

👉 Value must be provided

---

#### 🔗 **FOREIGN KEY**

```sql
user_id INT REFERENCES users(id)
```

👉 Links two tables

---

#### ✔️ **CHECK**

```sql
age INT CHECK (age >= 18)
```

👉 Validates condition

---

#### ⚙️ **DEFAULT**

```sql
status VARCHAR(20) DEFAULT 'active'
```

👉 Sets default value

---

### 🧠 Simple Example (All Together)

```sql
CREATE TABLE users (
  id INT PRIMARY KEY,
  name VARCHAR(50) NOT NULL,
  email VARCHAR(100) UNIQUE,
  age INT CHECK (age >= 18),
  status VARCHAR(20) DEFAULT 'active'
);
```


---

## ⛓️ **All SQL Constraints List**

### 🔑 **PRIMARY KEY**

* Uniquely identifies each row
* Cannot be `NULL`

---

### ⭐ **UNIQUE**

* Ensures all values are unique
* Allows `NULL` (usually)

---

### 🚫 **NOT NULL**

* Column must have a value
* No `NULL` allowed

---

### 🔗 **FOREIGN KEY**

* Links one table to another
* Maintains referential integrity

---

### ✔️ **CHECK**

* Validates data with a condition
* Example: `age >= 18`

---

### ⚙️ **DEFAULT**

* Assigns a default value
* Used when no value is provided

---

### 🧱 **AUTO_INCREMENT / IDENTITY**

* Automatically generates numbers
* Used for primary keys
* *(DB specific)*

---

### 📌 **INDEX** *(often asked with constraints)*

* Improves query performance
* Not a data rule, but related

---

## 🧠 Simple Example (All Constraints)

```sql
CREATE TABLE users (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(50) NOT NULL,
  email VARCHAR(100) UNIQUE,
  age INT CHECK (age >= 18),
  status VARCHAR(20) DEFAULT 'active',
  role_id INT,
  FOREIGN KEY (role_id) REFERENCES roles(id)
);
```

---
Perfect question 👍
I’ll explain **each part of the formula clearly, step-by-step**, with **meaning + memory trick**, no confusion.

---

## 📝 SQL Column Definition **Formula (Explained)**

```
column_name DATA_TYPE CONSTRAINTS EXTRA
```

Expanded:

```sql
column_name DATA_TYPE 
[PRIMARY KEY] [NOT NULL] [UNIQUE] [AUTO_INCREMENT] 
[DEFAULT value]
```

---

## 1️⃣ **column_name**

🔹 **What it means:**

* The **name of the column**
* Used to identify the data

🔹 **Rules:**

* Must be unique in the table
* No spaces
* Use meaningful names

🔹 **Example:**

```sql
id
email
created_at
```

🧠 Memory: **What do I call this data?**

---

## 2️⃣ **DATA_TYPE**

🔹 **What it means:**

* Defines **what kind of data** the column can store

🔹 **Common types:**

* `INT` → Numbers
* `VARCHAR(100)` → Text
* `DATE` → Date
* `BOOLEAN` → True/False

🔹 **Example:**

```sql
INT
VARCHAR(255)
```

🧠 Memory: **What type of data is it?**

---

## 3️⃣ **CONSTRAINTS** (Rules)

Constraints control **what values are allowed**.

---

### 🔑 **PRIMARY KEY**

🔹 Meaning:

* Uniquely identifies each row
* Cannot be `NULL`
* No duplicates

🔹 Example:

```sql
id INT PRIMARY KEY
```

🧠 Memory: **Main identity**

---

### 🚫 **NOT NULL**

🔹 Meaning:

* Value **must be provided**
* Column cannot be empty

🔹 Example:

```sql
name VARCHAR(50) NOT NULL
```

🧠 Memory: **Value is required**

---

### ⭐ **UNIQUE**

🔹 Meaning:

* No duplicate values allowed
* `NULL` allowed (usually)

🔹 Example:

```sql
email VARCHAR(100) UNIQUE
```

🧠 Memory: **Special but optional**

---

### 🔢 **AUTO_INCREMENT**

🔹 Meaning:

* Automatically generates numbers
* Used with primary keys

🔹 Example:

```sql
id INT AUTO_INCREMENT
```

🧠 Memory: **Number increases by itself**

---

## 4️⃣ **EXTRA**

---

### ⚙️ **DEFAULT value**

🔹 Meaning:

* Sets a value **automatically** if user doesn’t provide one

🔹 Example:

```sql
status VARCHAR(20) DEFAULT 'active'
```

🧠 Memory: **Fallback value**

---

## 🧠 FULL REAL EXAMPLE (Read Line by Line)

```sql
id INT PRIMARY KEY NOT NULL AUTO_INCREMENT
```

| Part           | Meaning     |
| -------------- | ----------- |
| id             | Column name |
| INT            | Number      |
| PRIMARY KEY    | Unique row  |
| NOT NULL       | Required    |
| AUTO_INCREMENT | Auto number |

---

## 🧠 **MASTER MEMORY TRICK** 🔥

### 👉 **N T C E**

* **N** → Name
* **T** → Type
* **C** → Constraints
* **E** → Extra

### 👉 **P N U A D** (Constraints order)

* **P** → Primary Key
* **N** → Not Null
* **U** → Unique
* **A** → Auto Increment
* **D** → Default

---

### 🎯 One-Line Interview Answer

> *A column is defined using its name, data type, constraints to control data, and extras like default or auto increment.*


<hr style="border: 2px solid green;">

<h2 id="What_is_NOT_NULL_Constraint" style="color:green; text-align:center;">  🚫 What is NOT NULL Constraint? </h2>


* **NOT NULL** ensures that a column **must have a value**
* It **does not allow NULL (empty) values**
* User **must provide data** for this column

---

### 🧠 Simple Example

```sql
name VARCHAR(50) NOT NULL
```

👉 `name` **cannot be empty**

---

### 📌 Real-Life Example

* 👤 User **must enter a name**
* 📧 Email **cannot be empty**
* 📅 Date of birth **required**

---

### ⚠️ Important Point

* `NOT NULL ≠ ''` (empty string)
* `NOT NULL` only prevents **NULL**, not empty text

---

### 🎯 One-Line Interview Answer

* **NOT NULL Constraint:**
  *NOT NULL ensures that a column always contains a value and cannot be left empty.*

---

### 🧠 Memory Trick

🚫 **NOT NULL = No Empty Allowed**


<hr style="border: 2px solid green;">

<h2 id="What_is_UNIQUE_Constraint" style="color:green; text-align:center;">  ⭐ What is UNIQUE Constraint? </h2>

* **UNIQUE** ensures that **no duplicate values** exist in a column
* Each value must be **different**
* `NULL` values are **allowed** (usually)

---

### 🧠 Simple Example

```sql
email VARCHAR(100) UNIQUE
```

👉 No two users can have the **same email**

---

### 📌 Real-Life Example

* 📧 Email ID
* 🆔 Username
* 🧾 Invoice number

---

### ⚠️ Important Points

* A table can have **multiple UNIQUE constraints**
* `PRIMARY KEY` = `UNIQUE + NOT NULL`
* `UNIQUE` ≠ `PRIMARY KEY`

---

### 🎯 One-Line Interview Answer

* **UNIQUE Constraint:**
  *UNIQUE ensures that all values in a column are different and prevents duplicate entries.*

---

### 🧠 Memory Trick

⭐ **UNIQUE = No Duplicates Allowed**




<hr style="border: 2px solid green;">

<h2 id="What_is_CHECK_Constraint" style="color:green; text-align:center;">  ✔️ What is CHECK Constraint? </h2>


* **CHECK** puts a **condition (rule)** on a column
* Only values that **satisfy the condition** are allowed
* Invalid values are **rejected**

---

### 🧠 Simple Example

```sql
age INT CHECK (age >= 18)
```

👉 Only ages **18 or above** are allowed

---

### 📌 Real-Life Examples

* 👶 Age must be **≥ 18**
* 💰 Salary must be **> 0**
* ⭐ Rating must be **1 to 5**

---

### 🎯 One-Line Interview Answer

* **CHECK Constraint:**
  *CHECK ensures that column values meet a specified condition.*

---

### 🧠 Memory Trick

✔️ **CHECK = Condition must be TRUE**


<hr style="border: 2px solid green;">

<h2 id="What_is_DEFAULT_Constraint" style="color:green; text-align:center;">  ⚙️ What is DEFAULT Constraint? </h2>


* **DEFAULT** sets a **predefined value** for a column
* If no value is provided, the **default value is used automatically**

---

### 🧠 Simple Example

```sql
status VARCHAR(20) DEFAULT 'active'
```

👉 If `status` is not given, it becomes **active**

---

### 📌 Real-Life Examples

* 🟢 Account status → `active`
* 📅 Created date → current date
* 🔢 Quantity → `1`

---

### 🎯 One-Line Interview Answer

* **DEFAULT Constraint:**
  *DEFAULT assigns an automatic value to a column when no value is provided.*

---

### 🧠 Memory Trick

⚙️ **DEFAULT = Auto value if missing**


<hr style="border: 2px solid green;">

<h1 style="text-align:center;" >Data Manipulation Language (DML)</h1>

<img  alt="Image" src="https://github.com/user-attachments/assets/f17a7aa4-937b-40cc-8e88-80e9d36fecf9" />

<h2 id="What_is_DML" style="color:green; text-align:center;">  ✍️ What is DML? </h2>

* **DML** stands for **Data Manipulation Language**
* Used to **work with data inside tables**
* It **adds, changes, deletes, and reads data**

---

### 🧰 Common DML Commands

* ➕ `INSERT` → Add new data
* ✏️ `UPDATE` → Modify existing data
* 🗑️ `DELETE` → Remove data
* 🔍 `SELECT` → Retrieve data

---

### 🧠 Simple Example



### 1️⃣ **INSERT** – Add new data

### 📌 Query

```sql
INSERT INTO users (name, email, age)
VALUES ('Rahul', 'rahul@gmail.com', 25);
```

### 🧠 Real Example

👉 A **new user registers** on a website

---

### 2️⃣ **SELECT** – Get data


```sql
SELECT name, email FROM users;

SELECT * FROM users WHERE age > 18;
```

👉 Show **name and email only**

---

### 3️⃣ **UPDATE** – Change existing data


```sql
UPDATE users
SET age = 26
WHERE email = 'rahul@gmail.com';
```

### 4️⃣ **DELETE** – Remove data

```sql
DELETE FROM users
WHERE id = 5;
```

## 🔁 DML with Real-Life Flow

```sql
-- Register user
INSERT INTO users (name, email) VALUES ('Amit', 'amit@gmail.com');

-- View profile
SELECT * FROM users WHERE email = 'amit@gmail.com';

-- Update profile
UPDATE users SET name = 'Amit Kumar' WHERE email = 'amit@gmail.com';

-- Delete account
DELETE FROM users WHERE email = 'amit@gmail.com';
```

---

### 🎯 One-Line Interview Answer

* **DML:**
  *DML is a set of SQL commands used to insert, update, delete, and retrieve data from tables.*

---

### 🧠 Memory Trick

✍️ **DML = Data Movement & Editing**



<hr style="border: 2px solid green;">

<h2 id="INSERT_and_INSERT_IGNORE" style="color:green; text-align:center;">  What is the difference between INSERT and INSERT IGNORE? </h2>

## ➕ **INSERT**

* Inserts **new data**
* ❌ Fails if there is a **duplicate key or constraint error**
* ⚠️ Query **stops with error**

### 📌 Example

```sql
INSERT INTO users (email)
VALUES ('john@gmail.com');
```

👉 Error if `email` already exists (UNIQUE)

---

## 🚫 **INSERT IGNORE** *(MySQL specific)*

* Inserts data **only if no error occurs**
* ✅ **Ignores duplicate & constraint errors**
* ⚠️ Problematic rows are **skipped**
* ❌ No error shown

### 📌 Example

```sql
INSERT IGNORE INTO users (email)
VALUES ('john@gmail.com');
```

👉 If email exists → **row is ignored**

---

## ⚖️ Difference Table

| Feature         | INSERT  | INSERT IGNORE   |
| --------------- | ------- | --------------- |
| Duplicate Entry | ❌ Error | ✅ Ignored       |
| Stops Execution | ✅       | ❌               |
| Error Message   | ✅       | ❌               |
| Data Inserted   | ❌       | ❌ (row skipped) |

---

## 🧠 Real-Life Example

* 🛑 **INSERT** → Stop signup if email exists
* 🚦 **INSERT IGNORE** → Skip duplicate silently

---

## 🎯 One-Line Interview Answer

* **INSERT vs INSERT IGNORE:**
  *INSERT throws an error on duplicates, while INSERT IGNORE skips duplicate records without error.*

---

### 🧠 Memory Trick

* ❌ **INSERT** → Strict
* 🚫 **IGNORE** → Skip errors


<hr style="border: 2px solid green;">

<h2 id="What_is_UPSERT" style="color:green; text-align:center;">  🔁 What is UPSERT? </h2>

<img alt="Image" src="https://github.com/user-attachments/assets/7fdf7bb7-d6a5-45ef-9091-1444cd508efe" />

* **UPSERT** = **UPDATE + INSERT**
* It **inserts a row if it does not exist**
* If the row **already exists**, it **updates it**

---

### 🧠 Simple Meaning

👉 **“Insert if new, update if exists”**

---

### 📌 Example (MySQL)

```sql
INSERT INTO users (email, name)
VALUES ('john@gmail.com', 'John')
ON DUPLICATE KEY UPDATE
name = 'John';
```

👉 If email exists → **UPDATE**
👉 If not → **INSERT**

---

### 📌 Example (PostgreSQL)

```sql
INSERT INTO users (email, name)
VALUES ('john@gmail.com', 'John')
ON CONFLICT (email)
DO UPDATE SET name = EXCLUDED.name;
```

---

### 🧠 Real-Life Example

* 🛒 Add product → update quantity if already in cart
* 👤 User login → create user if not exists

---

### ⚠️ Important Points

* Requires **UNIQUE or PRIMARY KEY**
* Syntax depends on database

---

### 🎯 One-Line Interview Answer

* **UPSERT:**
  *UPSERT inserts a record if it doesn’t exist, or updates it if it already exists.*

---

### 🧠 Memory Trick

🔁 **UPSERT = UPDATE + INSERT**



<hr style="border: 2px solid green;">

<h2 id="What_is_LIMIT" style="color:green; text-align:center;">  📏  What is LIMIT and ↪️ OFFSET? </h2>

### 📏 **What is LIMIT**

* **LIMIT** restricts the **number of rows returned**
* Used for **pagination** and performance

### 📌 Example

```sql
SELECT * FROM users
LIMIT 5;
```

👉 Returns **only 5 rows**

---

### ↪️ **What is OFFSET?**

* **OFFSET** skips a **number of rows**
* Used with `LIMIT` for pagination

### 📌 Example

```sql
SELECT * FROM users
LIMIT 5 OFFSET 5;
```

👉 Skips first 5 rows, shows **next 5**

---

### 🧠 Real-Life Example (Pagination)

* Page 1 → `LIMIT 10 OFFSET 0`
* Page 2 → `LIMIT 10 OFFSET 10`
* Page 3 → `LIMIT 10 OFFSET 20`

---

### ⚖️ Difference Table

| Feature    | LIMIT     | OFFSET    |
| ---------- | --------- | --------- |
| Purpose    | Row count | Skip rows |
| Used Alone | ✅         | ❌         |
| Pagination | ✅         | ✅         |

---

### 🎯 One-Line Interview Answer

* **LIMIT & OFFSET:**
  *LIMIT controls how many rows are returned, and OFFSET specifies how many rows to skip.*

---

### 🧠 Memory Trick

📏 **LIMIT = How many**
↪️ **OFFSET = From where**



<hr style="border: 2px solid green;">

<h2 id="What_is_ORDER_BY" style="color:green; text-align:center;">  🔃 What is ORDER BY? </h2>

* **ORDER BY** is used to **sort data**
* Sorts rows in **ascending or descending order**
* Default order is **ASC (ascending)**

---

### 📌 Simple Example

```sql
SELECT * FROM users
ORDER BY name;
```

👉 Sorts users **A → Z**

---

### 🔽 Descending Order

```sql
SELECT * FROM users
ORDER BY age DESC;
```

👉 Sorts ages **high → low**

---

### 🔢 Multiple Columns

```sql
SELECT * FROM users
ORDER BY age DESC, name ASC;
```

👉 First by age, then by name

---

### 🧠 Real-Life Example

* 📄 Sort users by **latest signup**
* 🏆 Rank students by **marks**

---

### 🎯 One-Line Interview Answer

* **ORDER BY:**
  *ORDER BY is used to sort query results in ascending or descending order.*

---

### 🧠 Memory Trick

🔃 **ORDER BY = Arrange data**

<hr style="border: 2px solid green;">

<h2 id="What_is_DISTINCT" style="color:green; text-align:center;">  🧹 What is DISTINCT </h2>

* **DISTINCT** removes **duplicate values**
* Returns **unique records only**
* Used with `SELECT`

---

## 📌 Simple Example

```sql
SELECT DISTINCT country FROM users;
```

👉 Shows each country **only once**

---

## 🧠 Real-Life Example

* 🌍 List of **unique cities**
* 📧 Unique email domains
* 🏷️ Unique categories

---

## ⚠️ Important Points

* Works on **selected columns**
* Multiple columns → unique **combination**

```sql
SELECT DISTINCT city, country FROM users;
```

---

## 🎯 One-Line Interview Answer

* **DISTINCT:**
  *DISTINCT is used to return unique values by removing duplicates from query results.*

---

## 🧠 Memory Trick

🧹 **DISTINCT = Remove duplicates**



<hr style="border: 2px solid green;">

<h2 id="What_is_Alias" style="color:green; text-align:center;">  🏷️ What is Alias (AS)? </h2>

* **Alias** is a **temporary name**
* Used for **columns or tables**
* Makes queries **shorter and more readable**
* Exists **only during the query**

---

## 📌 Column Alias Example

```sql
SELECT name AS full_name
FROM users;
```

👉 Shows column `name` as **full_name**

---

## 📌 Table Alias Example

```sql
SELECT u.name
FROM users AS u;
```

👉 `u` is a short name for `users`

---

## 🧠 Real-Life Example

* 🧾 Rename `SUM(amount)` as `total_sales`
* 🔍 Use short table names in joins

---

## ⚠️ Important Points

* `AS` is **optional**

```sql
SELECT name full_name FROM users;
```

* Alias does **not change actual column/table name**

---

## 🎯 One-Line Interview Answer

* **Alias (AS):**
  *Alias gives a temporary name to a table or column to make SQL queries more readable.*

---

## 🧠 Memory Trick

🏷️ **Alias = Nickname**


<hr style="border: 2px solid green;">

<h1 style="text-align:center;" > Aggregate Functions </h1>

<img  alt="Image" src="https://github.com/user-attachments/assets/9704bed3-427b-4708-b4ac-e2d543dfc5f2" />

<h2 id="What_are_Aggregate_Functions" style="color:green; text-align:center;">📊 What are Aggregate Functions? </h2>

* Aggregate functions **perform calculations on multiple rows**
* They return **one single value**
* Commonly used with **GROUP BY**

---

### 🔢 **COUNT()**

```sql
SELECT COUNT(*) FROM users;
```

👉 Counts total rows

---

### ➕ **SUM()**

```sql
SELECT SUM(salary) FROM employees;
```

👉 Total salary

---

### 📈 **AVG()**

```sql
SELECT AVG(age) FROM users;
```

👉 Average age

---

### 🔼 **MAX()**

```sql
SELECT MAX(marks) FROM students;
```

👉 Highest marks

---

### 🔽 **MIN()**

```sql
SELECT MIN(marks) FROM students;
```

👉 Lowest marks

---

### 🧠 Real-Life Examples

* 💰 Total sales
* 🧑 Average age
* 🏆 Highest score

---

### 🎯 One-Line Interview Answer

* **Aggregate Functions:**
  *Aggregate functions perform calculations on a set of rows and return a single result.*

---

## 🧠 Memory Trick

📊 **Aggregate = Group calculation**


<hr style="border: 2px solid green;">

<h2 id="What_is_GROUP_BY" style="color:green; text-align:center;"> 🧩 What is GROUP BY? </h2>


* **GROUP BY** groups rows that have **same values**
* Used with **aggregate functions**
* Returns **one result per group**

---

### 📌 Simple Example

```sql
SELECT department, COUNT(*)
FROM employees
GROUP BY department;
```

👉 Counts employees **per department**

---

### 🧠 Real-Life Examples

* 🏢 Employees per department
* 🌍 Users per country
* 🛒 Sales per product

---

### ⚠️ Important Rule (Interview 🔥)

> Any column in `SELECT` that is **not an aggregate** must be in `GROUP BY`

---

### 🎯 One-Line Interview Answer

* **GROUP BY:**
  *GROUP BY groups rows with the same values and is used with aggregate functions to summarize data.*

---

### 🧠 Memory Trick

🧩 **GROUP BY = Collect similar data**



<hr style="border: 2px solid green;">

<h2 id="What_is_HAVING" style="color:green; text-align:center;"> 🔍 What is HAVING? </h2>

* **HAVING** filters **grouped data**
* Used **after GROUP BY**
* Works with **aggregate functions**
* `WHERE` **cannot** be used with aggregates

---

### 📌 Simple Example

```sql
SELECT department, COUNT(*)
FROM employees
GROUP BY department
HAVING COUNT(*) > 5;
```

👉 Shows departments with **more than 5 employees**

---

### 🧠 Real-Life Example

* 🏢 Departments with high staff
* 🛒 Products with total sales > 100

---

### ⚠️ Key Difference (Interview 🔥)

* `WHERE` → filters **rows**
* `HAVING` → filters **groups**

---

### 🎯 One-Line Interview Answer

* **HAVING:**
  *HAVING is used to filter grouped results based on aggregate conditions.*

---

### 🧠 Memory Trick

🔍 **HAVING = Filter after GROUPING**



<hr style="border: 2px solid green;">

<h2 id="WHERE_vs_HAVING" style="color:green; text-align:center;"> 🔍 WHERE vs HAVING </h2>


### 📌 **WHERE**

* Filters **rows**
* Used **before GROUP BY**
* ❌ Cannot use aggregate functions

```sql
SELECT * FROM employees
WHERE salary > 30000;
```

👉 Filters individual employees

---

### 📌 **HAVING**

* Filters **groups**
* Used **after GROUP BY**
* ✅ Works with aggregate functions

```sql
SELECT department, COUNT(*)
FROM employees
GROUP BY department
HAVING COUNT(*) > 5;
```

👉 Filters departments

---

### ⚖️ Difference Table

| Feature             | WHERE                  | HAVING         |
| ------------------- | ---------------------- | -------------- |
| Filters             | Rows                   | Groups         |
| Used With           | SELECT, UPDATE, DELETE | GROUP BY       |
| Aggregate Functions | ❌                      | ✅              |
| Execution Order     | Before grouping        | After grouping |

---

### 🎯 One-Line Interview Answer

* **WHERE vs HAVING:**
  *WHERE filters individual rows, while HAVING filters grouped results after aggregation.*

---

### 🧠 Memory Trick

* 🔍 **WHERE** → Before grouping
* 🔍 **HAVING** → After grouping

<hr style="border: 2px solid green;">


<h1 style="text-align:center;" >Joins</h1>

<img  alt="Image" src="https://github.com/user-attachments/assets/aa154d67-6fc1-472e-a9d1-18d28c243bef" />

<h2 id="What_is_a_JOIN" style="color:green; text-align:center;"> 🔗 What is a JOIN? </h2>


* A **JOIN** combines data from **two or more tables**
* Tables are connected using a **common column**
* Used to get related data in **one result**

---

### 📌 Simple Example

```sql
SELECT users.name, orders.amount
FROM users
JOIN orders ON users.id = orders.user_id;
```

👉 Gets user names with their orders

---

### 🧠 Real-Life Example

* 👤 Users and their orders
* 🛒 Products and categories
* 🎓 Students and courses

---

### 🎯 One-Line Interview Answer

* **JOIN:**
  *JOIN is used to combine rows from multiple tables based on a related column.*

---

### 🧠 Memory Trick

🔗 **JOIN = Connect tables**


<hr style="border: 2px solid green;">

<h2 id="What_is_INNER_JOIN" style="color:green; text-align:center;"> 🔗 What is INNER JOIN (JOIN)? </h2>


* **INNER JOIN** returns **only matching records**
* Rows must match in **both tables**
* Non-matching rows are **excluded**

---

### 📌 Simple Example

```sql
SELECT users.name, orders.amount
FROM users
INNER JOIN orders ON users.id = orders.user_id;
```

```sql
SELECT users.name, orders.amount
FROM users
JOIN orders ON users.id = orders.user_id;
```

👉 Shows only users **who have orders**

---

### 🧠 Real-Life Example

* 👤 Customers with orders
* 🎓 Students enrolled in courses
* 🛒 Products that are sold

---

### 🎯 One-Line Interview Answer

* **INNER JOIN:**
  *INNER JOIN returns only the rows that have matching values in both tables.*

---

### 🧠 Memory Trick

🔗 **INNER = Common data only**


<hr style="border: 2px solid green;">

<h2 id="What_is_LEFT_JOIN" style="color:green; text-align:center;">⬅️ What is LEFT JOIN? </h2>

* **LEFT JOIN** returns **all records from the left table**
* Also returns **matching records from the right table**
* If no match exists, right-side columns are **NULL**

---

### 📌 Simple Example

```sql
SELECT users.name, orders.amount
FROM users
LEFT JOIN orders ON users.id = orders.user_id;
```

👉 Shows **all users**, even those **without orders**

---

### 🧠 Real-Life Example

* 👤 All customers + their orders (if any)
* 🎓 All students + their courses (if enrolled)

---

### 🎯 One-Line Interview Answer

* **LEFT JOIN:**
  *LEFT JOIN returns all rows from the left table and matching rows from the right table.*

---

### 🧠 Memory Trick

⬅️ **LEFT JOIN = Everything from left**


<hr style="border: 2px solid green;">

<h2 id="What_is_RIGHT_JOIN" style="color:green; text-align:center;"> ➡️ What is RIGHT JOIN? </h2>


* **RIGHT JOIN** returns **all records from the right table**
* Also returns **matching records from the left table**
* If no match exists, left-side columns are **NULL**

---

### 📌 Simple Example

```sql
SELECT users.name, orders.amount
FROM users
RIGHT JOIN orders ON users.id = orders.user_id;
```

👉 Shows **all orders**, even if user data is missing

---

### 🧠 Real-Life Example

* 🛒 All orders + customer details (if any)
* 🎓 All courses + enrolled students (if any)

---

### 🎯 One-Line Interview Answer

* **RIGHT JOIN:**
  *RIGHT JOIN returns all rows from the right table and matching rows from the left table.*

---

### 🧠 Memory Trick

➡️ **RIGHT JOIN = Everything from right**


<hr style="border: 2px solid green;">

<h2 id="What_is_FULL_OUTER_JOIN" style="color:green; text-align:center;"> 🔄 What is FULL OUTER JOIN? </h2>

* **FULL OUTER JOIN** returns **all records from both tables**
* Includes **matching and non-matching rows**
* Missing values are shown as **NULL**

---

### 📌 Simple Example

```sql
SELECT users.name, orders.amount
FROM users
FULL OUTER JOIN orders ON users.id = orders.user_id;
```

👉 Shows:

* Users with orders
* Users without orders
* Orders without users

---

### 🧠 Real-Life Example

* 👤 All users + their orders
* 🛒 All orders + customer info (even missing customers)

---

### ⚠️ Important Note

* ❌ **MySQL does not support FULL OUTER JOIN directly**
* Use `LEFT JOIN + RIGHT JOIN` with `UNION`

---

### 🎯 One-Line Interview Answer

* **FULL OUTER JOIN:**
  *FULL OUTER JOIN returns all rows from both tables, with NULLs where no match exists.*

---

### 🧠 Memory Trick

🔄 **FULL = Everything from both sides**


<hr style="border: 2px solid green;">


<h2 id="What_is_CROSS_JOIN" style="color:green; text-align:center;"> ❌➡️ What is CROSS JOIN? </h2>


* **CROSS JOIN** returns the **Cartesian product**
* Each row of the **first table** is combined with **each row of the second table**
* **No condition (ON clause)** is used

---

### 🧠 Simple Meaning

👉 **Every row × Every row**

---

## 📋 Example Tables (Real Data)

### 👤 **users and 🎨 colors**

| id | name  | id | color |  
| -- | ----- | -- | ----- |
| 1  | Rahul | 1  | Red   |
| 2  | Amit  | 2  | Blue  |
| 3  | Neha  | 3  | Green |

### 🔗 CROSS JOIN Query

```sql
SELECT users.name, colors.color
FROM users
CROSS JOIN colors;
```

---

### 📊 Result (3 × 3 = 9 rows)

| name  | color |
| ----- | ----- |
| Rahul | Red   |
| Rahul | Blue  |
| Rahul | Green |
| Amit  | Red   |
| Amit  | Blue  |
| Amit  | Green |
| Neha  | Red   |
| Neha  | Blue  |
| Neha  | Green |

---

### 🧠 Real-Life Example

* 👕 All **shirt sizes × colors**
* 📅 All **dates × time slots**
* 🧪 All **test cases combinations**

---

### 🎯 One-Line Interview Answer

* **CROSS JOIN:**
  *CROSS JOIN combines every row from one table with every row from another table.*

---

### 🧠 Memory Trick

❌ **No condition**
✖️ **Multiply rows**


<hr style="border: 2px solid green;">

<h2 id="What_is_SELF_JOIN" style="color:green; text-align:center;"> 🔁 What is SELF JOIN? </h2>


* **SELF JOIN** is a join where a table is joined **with itself**
* Used to compare rows **within the same table**
* Table aliases are **required**

---

## 🧠 Simple Meaning

👉 **A table talking to itself**

---

## 📋 Example Table (Employees)

| id | name  | manager_id |
| -- | ----- | ---------- |
| 1  | Rahul | NULL       |
| 2  | Amit  | 1          |
| 3  | Neha  | 1          |

---

## 🔗 SELF JOIN Query

```sql
SELECT e.name AS employee, m.name AS manager
FROM employees e
JOIN employees m
ON e.manager_id = m.id;
```

---

## 📊 Result

| employee | manager |
| -------- | ------- |
| Amit     | Rahul   |
| Neha     | Rahul   |

👉 Rahul has no manager, so not shown

---

## 🧠 Real-Life Examples

* 👨‍💼 Employee–Manager relationship
* 🌳 Category–Subcategory
* 💬 Comment–Reply system

---

## 🎯 One-Line Interview Answer

* **SELF JOIN:**
  *SELF JOIN is a join where a table is joined with itself to compare related rows.*

---

## 🧠 Memory Trick

🔁 **SELF JOIN = Same table twice**


<hr style="border: 2px solid green;">

<h2 id="Difference_between_JOIN_and_SUBQUERY" style="color:green; text-align:center;"> Difference between JOIN and SUBQUERY? </h2>


## 🔗 **JOIN**

* Combines **multiple tables side-by-side**
* Usually **faster** and more readable
* Used when you need **columns from multiple tables**

### 📌 Example

```sql
SELECT u.name, o.amount
FROM users u
JOIN orders o ON u.id = o.user_id;
```

👉 Shows users with their orders

---

## 🔍 **SUBQUERY**

* A **query inside another query**
* Runs **first** and passes result to outer query
* Used for **filtering or comparison**

### 📌 Example

```sql
SELECT name
FROM users
WHERE id IN (
  SELECT user_id FROM orders
);
```

👉 Shows users who have orders

---

## ⚖️ Difference Table

| Feature     | JOIN                    | SUBQUERY             |
| ----------- | ----------------------- | -------------------- |
| Structure   | Side-by-side tables     | Query inside query   |
| Performance | Usually faster          | Can be slower        |
| Readability | Clear for relationships | Clear for conditions |
| Use Case    | Fetch related columns   | Filter data          |

---

## 🧠 Real-Life Thinking

* 🔗 **JOIN** → “Get user name + order amount”
* 🔍 **SUBQUERY** → “Get users who have orders”

---

## 🎯 One-Line Interview Answer

* **JOIN vs SUBQUERY:**
  *JOIN combines data from multiple tables, while a subquery is a query inside another query used for filtering or comparison.*

---

## 🧠 Memory Trick

* 🔗 **JOIN** = Combine tables
* 🔍 **SUBQUERY** = Query inside query


<hr style="border: 2px solid green;">


<h1 style="text-align:center;" >Subqueries</h1>

<img  alt="Image" src="https://github.com/user-attachments/assets/0c8bcbcf-595f-4c83-b1c5-3757a08581b2" />

<h2 id="What_is_a_Subquery" style="color:green; text-align:center;">🔍 What is a Subquery? </h2>

* A **subquery** is a **query inside another SQL query**
* The **inner query runs first**
* Its result is used by the **outer query**

---

## 🧠 Simple Meaning

👉 **Query inside a query**

---

## 📌 Example

### Get users who have orders

```sql
SELECT name
FROM users
WHERE id IN (
  SELECT user_id FROM orders
);
```

---

## 🧠 Real-Life Example

* 🎓 Students who passed an exam
* 🛒 Customers who placed orders
* 👨‍💼 Employees earning more than average salary

---

## 🎯 One-Line Interview Answer

* **Subquery:**
  *A subquery is a query inside another query whose result is used by the main query.*

---

## 🧠 Memory Trick

🔍 **Subquery = Inside query**


<hr style="border: 2px solid green;">

<h2 id="Types_of_Subqueries_in_SQL" style="color:green; text-align:center;"> 🔍 Types of Subqueries in SQL </h2>

<img  alt="Image" src="https://github.com/user-attachments/assets/cc42e0c2-2c8d-4848-a636-e546b6e66509" />

## 1️⃣ **Single-Row Subquery**

* Returns **one row**
* Uses `=`, `<`, `>`

### 📌 Example

```sql
SELECT name
FROM employees
WHERE salary > (
  SELECT AVG(salary) FROM employees
);
```

### 🎯 Interview Answer

👉 *Returns only one row*

---

## 2️⃣ **Multiple-Row Subquery**

* Returns **multiple rows**
* Uses `IN`, `ANY`, `ALL`

### 📌 Example

```sql
SELECT name
FROM employees
WHERE department_id IN (
  SELECT id FROM departments
);
```

### 🎯 Interview Answer

👉 *Returns more than one row*

---

## 3️⃣ **Multiple-Column Subquery**

* Returns **multiple columns**
* Used with row comparison

### 📌 Example

```sql
SELECT *
FROM orders
WHERE (user_id, amount) IN (
  SELECT user_id, MAX(amount)
  FROM orders
  GROUP BY user_id
);
```

### 🎯 Interview Answer

👉 *Returns multiple columns*

---

## 4️⃣ **Correlated Subquery**

* Depends on **outer query**
* Runs **once per row**

### 📌 Example

```sql
SELECT name
FROM employees e
WHERE salary > (
  SELECT AVG(salary)
  FROM employees
  WHERE department_id = e.department_id
);
```

### 🎯 Interview Answer

👉 *Uses outer query values*

---

## 5️⃣ **Scalar Subquery**

* Returns **single value**
* Can be used in `SELECT`

### 📌 Example

```sql
SELECT name,
       (SELECT COUNT(*) FROM orders) AS total_orders
FROM users;
```

### 🎯 Interview Answer

👉 *Returns one value*

---

## 6️⃣ **Nested Subquery**

* Subquery inside **another subquery**

### 📌 Example

```sql
SELECT name
FROM users
WHERE id IN (
  SELECT user_id
  FROM orders
  WHERE product_id IN (
    SELECT id FROM products
  )
);
```

### 🎯 Interview Answer

👉 *Subquery inside another subquery*

---

## 🧠 Easy Memory Table

| Type         | Memory Hint      |
| ------------ | ---------------- |
| Single-row   | One result       |
| Multi-row    | Many results     |
| Multi-column | Many columns     |
| Correlated   | Depends on outer |
| Scalar       | Single value     |
| Nested       | Inside inside    |

---

## 🧠 One-Line Master Interview Answer

> *Subqueries can be single-row, multi-row, multi-column, correlated, scalar, or nested.*

<hr style="border: 2px solid green;">

<h1 style="text-align:center;" >Set Operations</h1>

<hr style="border: 2px solid green;">


<img  alt="Image" src="https://github.com/user-attachments/assets/b3449810-8246-4b06-970d-88b6bebf8b53" />

<h2 id="What_is_UNION" style="color:green; text-align:center;"> 🔗 What is UNION? </h2>

* **UNION** is used to **combine results of two or more SELECT queries**
* Removes **duplicate rows** by default
* All SELECT queries must have:

  * Same number of columns
  * Same data types
  * Same column order

---

### 🧠 Simple Meaning

👉 **Add query results together (no duplicates)**

---

### 📋 Simple Example

| **students_2024** |   | **students_2025** |
| ----------------- | - | ----------------- |
| name              |   | name              |
| Rahul             |   | Amit              |
| Amit              |   | Neha              |

---

### UNION Query

```sql
SELECT name FROM students_2024
UNION
SELECT name FROM students_2025;
```

---

### Result

| name  |
| ----- |
| Rahul |
| Amit  |
| Neha  |

---

### 🧠 Real-Life Example

* 📚 Students from multiple years
* 🏢 Employees from different branches

---

### 🎯 One-Line Interview Answer

* **UNION:**
  *UNION combines results of multiple SELECT queries and removes duplicate records.*

---

### 🧠 Memory Trick

➕ **UNION = Merge + remove duplicates**



<hr style="border: 2px solid green;">

<h2 id="What_is_UNION_ALL" style="color:green; text-align:center;"> 🔗 What is UNION ALL? </h2>

* **UNION ALL** combines results of multiple `SELECT` queries
* **Does NOT remove duplicates**
* Faster than `UNION`

---

### 🧠 Simple Meaning

👉 **Add everything (duplicates included)**

---

### 📋 Simple Example

### Table: `students_2024` and `students_2025`

| name  | | name |
| ----- |-| ---- |
| Rahul | | Amit |
| Amit  | | Neha |


### UNION ALL Query

```sql
SELECT name FROM students_2024
UNION ALL
SELECT name FROM students_2025;
```
---

### Result

| name  |
| ----- |
| Rahul |
| Amit  |
| Amit  |
| Neha  |

---

### ⚖️ UNION vs UNION ALL

| Feature           | UNION  | UNION ALL |
| ----------------- | ------ | --------- |
| Remove duplicates | ✅ Yes  | ❌ No      |
| Performance       | Slower | Faster    |

---

### 🎯 One-Line Interview Answer

* **UNION ALL:**
  *UNION ALL combines results of multiple SELECT queries without removing duplicates.*

---

### 🧠 Memory Trick

➕➕ **ALL = Everything stays**


<hr style="border: 2px solid green;">

<h2 id="What_is_INTERSECT" style="color:green; text-align:center;"> What is INTERSECT? </h2>


* **INTERSECT** returns **only common rows** between two `SELECT` queries
* Removes duplicates automatically
* Both queries must have:

  * Same number of columns
  * Same data types
  * Same column order

---

### 🧠 Simple Meaning

👉 **Common data only**

---

## 📋 Simple Example

### Table: `students_2024` and `students_2025`

| name (students_2024) | | name (students_2025) |
| ----- |-| ----- |
| Rahul | | Amit  |
| Amit  | | Neha  |
| Neha  | | Priya |

---

### INTERSECT Query

```sql
SELECT name FROM students_2024
INTERSECT
SELECT name FROM students_2025;
```

### Result

| name |
| ---- |
| Amit |
| Neha |

---

### 🧠 Real-Life Example

* 🎓 Students enrolled in both years
* 🛒 Products sold in two stores

---

### 🎯 One-Line Interview Answer

* **INTERSECT:**
  *INTERSECT returns only the common records between two SELECT queries.*

---

### 🧠 Memory Trick

🔗 **INTERSECT = Intersection (common part)**

⚠️ **Note:**

* Not supported in **MySQL** (use `INNER JOIN` instead)


<hr style="border: 2px solid green;">

<h2 id="What_is_EXCEPT_MINUS" style="color:green; text-align:center;"> 🔗 What is EXCEPT / MINUS? </h2>

* **EXCEPT** (or **MINUS** in Oracle) returns rows that are:

  * Present in the **first query**
  * BUT **not present** in the second query
* Removes duplicates automatically

---

## 🧠 Simple Meaning

👉 **First − Second**

---

### Table: `students_2024` and  `students_2025`

| name (students_2024) | | name (students_2025) |
| ----- |-| ----- |
| Rahul | | Amit  |
| Amit  | | Neha  |
| Neha  | | Priya |


### EXCEPT Query

```sql
SELECT name FROM students_2024
EXCEPT
SELECT name FROM students_2025;
```
---

### Result

| name  |
| ----- |
| Rahul |

---

## 🧠 Oracle Version (MINUS)

```sql
SELECT name FROM students_2024
MINUS
SELECT name FROM students_2025;
```
---

## ⚠️ Important Notes

* ❌ Not supported in **MySQL**
* ✔ Supported in **PostgreSQL, SQL Server, Oracle**

---

## 🎯 One-Line Interview Answer

* **EXCEPT / MINUS:**
  *Returns rows from the first query that are not present in the second query.*

---

## 🧠 Memory Trick

➖ **EXCEPT = Remove second from first**


<hr style="border: 2px solid green;">

<h1 style="text-align:center;" >Indexes</h1>

<img  alt="Image" src="https://github.com/user-attachments/assets/f3e71566-2133-4c0b-bf0b-87def719e4ec" />

<hr style="border: 2px solid green;">

<h2 id="What_is_an_Index" style="color:green; text-align:center;"> 📌 What is an Index? </h2>

* An **index** is a database object that **speeds up data searching**
* Works like a **book index**
* Makes `SELECT` queries faster

---

### 🧠 Simple Meaning

👉 **Index = Fast search**

---

### 📋 Simple Example

### Without Index

```sql
SELECT * FROM users WHERE email = 'test@gmail.com';
```

👉 Database scans **all rows**

---

### Create Index

```sql
CREATE INDEX idx_email ON users(email);
```

---

### With Index

👉 Database finds data **quickly**

---

### 🧠 Real-Life Example

📘 Book index → jump to page
🗂️ Database index → jump to row

---

### ⚠️ Important Notes

* Index **improves SELECT**
* Index **slows INSERT / UPDATE / DELETE**
* Uses **extra storage**
---

### 🎯 One-Line Interview Answer

* **Index:**
  *An index improves query performance by allowing faster data retrieval.*
---

### 🧠 Memory Trick

⚡ **Index = Speed**

<hr style="border: 2px solid green;">

<h2 id="Types_of_Indexes_in_SQL" style="color:green; text-align:center;"> Types of Indexes in SQL </h2>



### 1️⃣ **PRIMARY INDEX**

* Created automatically for **PRIMARY KEY**
* Values are **unique & not NULL**

```sql
PRIMARY KEY (id)
```

🎯 *Index for primary key*

---

### 2️⃣ **UNIQUE INDEX**

* Ensures **no duplicate values**

```sql
CREATE UNIQUE INDEX idx_email ON users(email);
```

🎯 *Prevents duplicates*

---

### 3️⃣ **NORMAL (NON-UNIQUE) INDEX**

* Allows duplicate values
* Improves search speed

```sql
CREATE INDEX idx_name ON users(name);
```

🎯 *Speeds up queries*

---

### 4️⃣ **COMPOSITE INDEX**

* Index on **multiple columns**

```sql
CREATE INDEX idx_name_email ON users(name, email);
```

🎯 *Index on more than one column*

---

### 5️⃣ **FULL-TEXT INDEX**

* Used for **text searching**

```sql
CREATE FULLTEXT INDEX idx_desc ON products(description);
```

🎯 *Used for keyword search*

---

### 6️⃣ **CLUSTERED INDEX**

* Data is **physically stored** in index order
* Only **one per table**

🎯 *Controls physical data order*

---

### 7️⃣ **NON-CLUSTERED INDEX**

* Index stored **separately** from data
* Multiple allowed

🎯 *Index separate from table*

---

### 🧠 Easy Memory Table

| Index Type    | Memory Hint      |
| ------------- | ---------------- |
| PRIMARY       | Main ID          |
| UNIQUE        | No duplicates    |
| NORMAL        | Speed only       |
| COMPOSITE     | Multiple columns |
| FULL-TEXT     | Text search      |
| CLUSTERED     | Physical order   |
| NON-CLUSTERED | Separate index   |

---

### 🧠 One-Line Master Interview Answer

> *Indexes can be primary, unique, normal, composite, full-text, clustered, and non-clustered.*



<hr style="border: 2px solid green;">

<h1 style="text-align:center;" >Transactions</h1>

<hr style="border: 2px solid green;">


<img  alt="Image" src="https://github.com/user-attachments/assets/20c0da0f-f603-425a-812b-10189aa791d0" />

<h2 id="What_is_a_Transaction" style="color:green; text-align:center;"> 🔄 What is a Transaction? </h2>

* A **transaction** is a **group of SQL operations** executed as **one unit**
* Either **all succeed** or **all fail**
---

### 🧠 Simple Meaning

👉 **All or nothing**

---

### 📋 Simple Example

```sql
START TRANSACTION;

INSERT INTO orders (user_id, amount) VALUES (1, 500);
UPDATE users SET balance = balance - 500 WHERE id = 1;

COMMIT;
```

👉 Both queries succeed together

---

### ❌ If Error Occurs

```sql
ROLLBACK;
```

👉 Changes are undone

---

### 🧠 Real-Life Example

🏦 Bank transfer
➕ Debit one account
➕ Credit another
👉 Both must succeed

---

### 🎯 One-Line Interview Answer

* **Transaction:**
  *A transaction is a set of SQL operations that execute as a single unit, ensuring data consistency.*

---

### 🧠 Memory Trick

🔄 **Transaction = All or nothing**


<hr style="border: 2px solid green;">

<h2 id="What_is_COMMIT" style="color:green; text-align:center;"> ✅ What is COMMIT? </h2>


* **COMMIT** permanently **saves all changes** made in a transaction
* After COMMIT, changes **cannot be undone**

---

### 🧠 Simple Meaning

👉 **Save changes forever**

---

### 📋 Simple Example

```sql
START TRANSACTION;

INSERT INTO users (name) VALUES ('Rahul');

COMMIT;
```

👉 Data is saved permanently

---

### ❌ Without COMMIT

```sql
ROLLBACK;
```

👉 Changes are canceled

---

### 🧠 Real-Life Example

💾 Clicking **Save** in a document

---

### 🎯 One-Line Interview Answer

* **COMMIT:**
  *COMMIT saves all transaction changes permanently in the database.*

---

### 🧠 Memory Trick

💾 **COMMIT = Confirm & Save**



<hr style="border: 2px solid green;">

<h2 id="What_is_ROLLBACK" style="color:green; text-align:center;"> ❌ What is ROLLBACK? </h2>

* **ROLLBACK** cancels all changes made in a transaction
* Database returns to the **previous state**
* Used when an **error occurs**

---

### 🧠 Simple Meaning

👉 **Undo changes**

---

### 📋 Simple Example

```sql
START TRANSACTION;

UPDATE users SET balance = balance - 500 WHERE id = 1;

ROLLBACK;
```

👉 Balance change is undone

---

### 🧠 Real-Life Example

↩️ **Undo (Ctrl + Z)**

---

### 🎯 One-Line Interview Answer

* **ROLLBACK:**
  *ROLLBACK undoes all changes made in a transaction.*

---

### 🧠 Memory Trick

↩️ **ROLLBACK = Go back**


<hr style="border: 2px solid green;">

<h2 id="What_is_SAVEPOINT" style="color:green; text-align:center;">📍📍📍 What is SAVEPOINT? </h2>

<img alt="Image" src="https://github.com/user-attachments/assets/2e14ed5f-25a9-4063-928f-d4f471667376" />

* **SAVEPOINT** creates a **checkpoint inside a transaction**
* You can **ROLLBACK to a specific point**, not the whole transaction

---

### 🧠 Simple Meaning

👉 **Transaction bookmark**

---

### 📋 Simple Example

```sql
START TRANSACTION;

INSERT INTO users (name) VALUES ('Amit');
SAVEPOINT sp1;

INSERT INTO users (name) VALUES ('Neha');

ROLLBACK TO sp1;
COMMIT;
```

👉 Only **Amit** is saved, **Neha** is undone

---

### 🧠 Real-Life Example

📝 Editing document → undo to a point

---

### 🎯 One-Line Interview Answer

* **SAVEPOINT:**
  *SAVEPOINT allows partial rollback within a transaction.*

---

### 🧠 Memory Trick

📍 **SAVEPOINT = Mark a point**


<hr style="border: 2px solid green;">

<h2 id="What_are_ACID_Properties" style="color:green; text-align:center;"> 🧪 What are ACID Properties? </h2>

![Image](https://github.com/user-attachments/assets/7ebe97cb-cd6e-445f-ac94-5606d79a3e8a)

ACID ensures that **database transactions are reliable and safe**

---

### 🅰️ **A – Atomicity**

* Transaction is **all or nothing**
* If one step fails, everything fails

**Example:**
Bank transfer fails → money not deducted

🎯 *All operations succeed or none*

---

### 🅲 **C – Consistency**

* Database moves from **one valid state to another**
* Rules & constraints are maintained

**Example:**
Balance never becomes negative

🎯 *Data remains valid*

---

### 🅸 **I – Isolation**

* Multiple transactions **don’t affect each other**
* Appears like transactions run one-by-one

**Example:**
Two users booking same seat

🎯 *Transactions are isolated*

---

### 🅳 **D – Durability**

* Once committed, data is **permanently saved**
* Survives power failure or crash

**Example:**
Saved bank transfer remains after crash

🎯 *Data stays forever after commit*

---

### 🧠 Easy Memory Trick 🔥

👉 **ACID = Always Correct In Database**

---

### 🎯 One-Line Interview Answer

> *ACID properties ensure transactions are atomic, consistent, isolated, and durable.*

