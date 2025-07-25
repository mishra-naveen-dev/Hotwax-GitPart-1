##  SQL Overview

###  What is Data?
Data → A set of meaningful information  
**Example:** `"Naveen", 22, "Indore"`

---

###  What is a Database?
A **database** is an organized collection of structured data, stored electronically for easy access, management, and updating.

Example Table:

| ID | Name   | Age | City    |
|----|--------|-----|---------|
| 1  | Naveen | 22  | Indore  |
| 2  | Neeraj | 21  | -       |

---

###  What is SQL?
**SQL (Structured Query Language)** is used to access, manipulate, and manage data in a relational database.

- It is a **DSL (Domain-Specific Language)** – used for a specific domain (RDBMS).
- It is declarative – focus on **what** you want, not **how**.

---

###  Programming Paradigms:
- **Declarative Language:** Focuses on *what* to do  
- **Functional Language:** Focuses on *functions* without changing state

---

###  Query vs Statement
- **Query:** Retrieves data (e.g., `SELECT * FROM students;`)
- **Statement:** Any SQL instruction, including DDL, DML, and queries

---

###  ACID Properties in DBMS
1. **A - Atomicity**: All operations in a transaction happen completely or not at all  
2. **C - Consistency**: Database remains consistent after a transaction  
3. **I - Isolation**: Transactions occur independently  
4. **D - Durability**: Changes persist even after system failure

**Isolation Levels:**
- Read Uncommitted
- Read Committed
- Repeatable Read
- Serializable

---

###  Primary Key vs Foreign Key
| Primary Key       | Foreign Key              |
|-------------------|--------------------------|
| Uniquely identifies a record | Refers to primary key in another table |
| Cannot be NULL     | Can contain duplicates & NULLs |
| One per table       | Can be multiple |

---

###  DML vs DDL
| DML (Data Manipulation) | DDL (Data Definition) |
|-------------------------|------------------------|
| Deals with data         | Deals with structure   |
| `SELECT`, `INSERT`, `UPDATE`, `DELETE` | `CREATE`, `ALTER`, `DROP`, `TRUNCATE` |

---

###  TRUNCATE vs DELETE vs DROP
| Operation | Removes | Rollback | Resets Identity | Speed |
|-----------|---------|----------|------------------|-------|
| DELETE    | Rows    |  Yes   |  No             | Slow  |
| TRUNCATE  | All Rows|  No    |  Yes            | Fast  |
| DROP      | Table   | No    |  Yes            | Very Fast |

---

###  Normalization (3NF Example)
**Normalization** helps in reducing redundancy and improving data integrity.

#### Example:

Unnormalized Table:
| StudentID | Name   | Course     |
|-----------|--------|------------|
| 1         | Naveen | HTML       |
| 1         | Naveen | CSS        |

**1NF** – Remove repeating groups  
**2NF** – Move partial dependencies to separate tables  
**3NF** – Remove transitive dependency

Result (3NF):
- Student Table: `StudentID`, `Name`
- Course Table: `CourseID`, `CourseName`
- Enrollment Table: `StudentID`, `CourseID`
