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

## 🧱 CREATE DATABASE

```sql
CREATE DATABASE school;
```

👉 Creates a new database named **school**

---

## 🗄️ CREATE TABLE

```sql
CREATE TABLE students (
  id INT PRIMARY KEY,
  name VARCHAR(50),
  age INT
);
```

👉 Creates a **students** table

---

## ✏️ ALTER TABLE (Add Column)

```sql
ALTER TABLE students
ADD email VARCHAR(100);
```

👉 Adds a new column **email**

---

## ✏️ ALTER TABLE (Modify Column)

```sql
ALTER TABLE students
MODIFY age SMALLINT;
```

👉 Changes column data type

---

## 🗑️ DROP TABLE

```sql
DROP TABLE students;
```

👉 Deletes the table completely

---

## 🚿 TRUNCATE TABLE

```sql
TRUNCATE TABLE students;
```

👉 Deletes all rows, keeps structure

---

## 🏷️ CREATE INDEX

```sql
CREATE INDEX idx_name
ON students(name);
```

👉 Improves search speed on **name**

---

## 🏷️ CREATE UNIQUE INDEX

```sql
CREATE UNIQUE INDEX idx_email
ON students(email);
```

👉 Ensures **email is unique**

---

## ❌ DROP INDEX

```sql
DROP INDEX idx_name;
```

👉 Removes the index

---

## 🧠 One-Line Interview Summary

* **CREATE** → Makes database/table
* **ALTER** → Changes structure
* **DROP** → Deletes structure
* **TRUNCATE** → Clears data
* **INDEX** → Speeds up search

---

### 📌 Memory Trick

🏗️ Build → ✏️ Change → 🚿 Clean → 💣 Remove → ⚡ Speed

If you want next, I can give:

* ✅ **DML examples (INSERT, UPDATE, DELETE, SELECT)**
* ✅ **Real interview practice questions**
* ✅ **Laravel-friendly SQL examples**


---

### 🎯 One-Line Interview Answer

* **DDL:**
  *DDL is a set of SQL commands used to define and manage the structure of database objects.*


<span style="color:green;">================================================================ </span>

<h2 id="IIIIIIIIIIIIIIIIIIIIII" style="color:green">  GGGGGGGGGGGGGGGGGGGGGGGGGGGG </h2>



<span style="color:green;">================================================================ </span>

<h2 id="IIIIIIIIIIIIIIIIIIIIII" style="color:green">  GGGGGGGGGGGGGGGGGGGGGGGGGGGG </h2>
