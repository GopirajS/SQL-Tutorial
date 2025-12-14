<span style="color:green;">================================================================ </span>

<h1 style="text-align:center;" >Set Operations</h1>

<h2 id="What_is_UNION" style="color:green"> 🔗 What is UNION? </h2>

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



<span style="color:green;">================================================================ </span>

<h2 id="What_is_UNION_ALL" style="color:green"> 🔗 What is UNION ALL? </h2>

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


<span style="color:green;">================================================================ </span>

<h2 id="What_is_INTERSECT" style="color:green"> What is INTERSECT? </h2>


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


<span style="color:green;">================================================================ </span>

<h2 id="What_is_EXCEPT_MINUS" style="color:green"> 🔗 What is EXCEPT / MINUS? </h2>

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
