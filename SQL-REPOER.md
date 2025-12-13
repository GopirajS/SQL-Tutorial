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


<span style="color:green;">================================================================ </span>

<h1 style="text-align:center;" >SQL Basics</h1>

![Image](https://github.com/user-attachments/assets/6c1a0e04-7bc4-4fd1-8917-a3195089cd3d)

<h2 id="What_is_SQL_and_why_is_it_used" style="color:green">What is SQL and why is it used?</h2>

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



<span style="color:green;">================================================================ </span>

<h2 id="D_between_SQL_MySQL_PostgreSQL_and_SQLite" style="color:green">What are the differences between SQL, MySQL, PostgreSQL, and SQLite?</h2>


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


<span style="color:green;">================================================================ </span>

<h2 id="primary_foreign_Unique_Key" style="color:green">What is a primary key ,foreign key and Unique Key</h2>

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


<span style="color:green;">================================================================ </span>

<h2 id="What_is_a_NULL_value" style="color:green">What is a NULL value?</h2>


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


<span style="color:green;">================================================================ </span>

<h2 id="DB_DELETE_TRUNCATE_and_DROP" style="color:green">What is the difference between DELETE, TRUNCATE, and DROP?</h2>


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



<span style="color:green;">================================================================ </span>

<h2 id="What_)is_)a_)Schema" style="color:green">What is a Schema?</h2>

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


<span style="color:green;">================================================================ </span>

<h2 id="What_are_Data_Types_in_SQL" style="color:green">🧾 What are Data Types in SQL?</h2>

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


<span style="color:green;">================================================================ </span>


<h1 style="text-align:center;" >Data Definition Language (DDL)</h1>

<h2 id="What_is_DDL" style="color:green">  🏗️ What is DDL? </h2>

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


<span style="color:green;">================================================================ </span>

<h2 id="What_are_Constraints" style="color:green">  ⛓️ What are Constraints? </h2>

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


<span style="color:green;">================================================================ </span>

<h2 id="What_is_NOT_NULL_Constraint" style="color:green">  🚫 What is NOT NULL Constraint? </h2>


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


<span style="color:green;">================================================================ </span>

<h2 id="What_is_UNIQUE_Constraint" style="color:green">  ⭐ What is UNIQUE Constraint? </h2>

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




<span style="color:green;">================================================================ </span>

<h2 id="What_is_CHECK_Constraint" style="color:green">  ✔️ What is CHECK Constraint? </h2>


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


<span style="color:green;">================================================================ </span>

<h2 id="What_is_DEFAULT_Constraint" style="color:green">  ⚙️ What is DEFAULT Constraint? </h2>


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
