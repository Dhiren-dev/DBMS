# Database Management Systems (DBMS) Lab Experiments (1 to 9)

A comprehensive, self-contained repository of practical DBMS laboratory experiments tested on **MySQL 8.0+**. This repository contains complete schemas, constraints, DDL, DML, DCL, TCL, joins, views, triggers, and concurrency control experiments organized across 4 dedicated folders matching academic syllabus requirements.

Each file is directly named with the specific database operation it performs for rapid reference and automated evaluation.

---

## 📁 Repository Structure

```
DBMS/
├── 01_Easy_Separate_Examples/      # Independent scenarios (Library, Shop, Bank, School, Office, Store, Wallet)
│   ├── 01_database_creation.txt                # Exp 1: Basic Database Creation (Library)
│   ├── 02_er_to_relational_mapping.txt         # Exp 2: ER/EER to Relational Schema (Library)
│   ├── 03_ddl_and_integrity_constraints.txt   # Exp 3: DDL and Integrity Constraints (Shop)
│   ├── 04_dml_insert_update_delete.txt         # Exp 4: DML - Insert, Update, Delete (Bank Account)
│   ├── 05_dcl_grant_and_revoke.txt            # Exp 5: DCL - User Permissions & Roles (School)
│   ├── 06_queries_and_aggregate_functions.txt  # Exp 6: SQL Queries & Aggregate Functions (Employee)
│   ├── 07_join_operations.txt                 # Exp 7: Join Operations (Customer & Orders)
│   ├── 08_views_and_triggers.txt               # Exp 8: Views & Triggers (Product Audit Log)
│   └── 09_transactions_and_concurrency.txt    # Exp 9: Transactions & Concurrency Control (Wallet)
│
├── 02_Student_College_FULL_v1/     # Comprehensive Student-College schema with full constraints (Set 1)
│   ├── 01_database_creation.txt                # Exp 1: Complete Student-College Database
│   ├── 02_er_to_relational_mapping.txt         # Exp 2: Map ER/EER Model to Relations
│   ├── 03_ddl_and_integrity_constraints.txt   # Exp 3: DDL and Table Alterations
│   ├── 04_dml_insert_update_delete.txt         # Exp 4: DML Operations (Insert/Update/Delete)
│   ├── 05_dcl_grant_and_revoke.txt            # Exp 5: DCL Grant and Revoke Commands
│   ├── 06_queries_and_aggregate_functions.txt  # Exp 6: Select Queries & Aggregate Calculations
│   ├── 07_join_operations.txt                 # Exp 7: Join Types (Inner, Non-Equi, Self, Outer, Cross)
│   ├── 08_views_and_triggers.txt               # Exp 8: Create View and Audit Triggers
│   └── 09_transactions_and_concurrency.txt    # Exp 9: Commit, Rollback and Row Locking
│
├── 03_Student_College_FULL_v2/     # Comprehensive Student-College schema (Set 2 / Academic variant)
│   ├── 01_database_creation.txt                # Exp 1: Complete College Relational Database
│   ├── 02_er_to_relational_mapping.txt         # Exp 2: Relational Mapping (M:N Relations)
│   ├── 03_ddl_and_integrity_constraints.txt   # Exp 3: Integrity Constraints & Table Mutations
│   ├── 04_dml_insert_update_delete.txt         # Exp 4: Data Manipulation Statements
│   ├── 05_dcl_grant_and_revoke.txt            # Exp 5: Security Grant & Revoke Matrix
│   ├── 06_queries_and_aggregate_functions.txt  # Exp 6: Grouping, Filtering & Aggregation
│   ├── 07_join_operations.txt                 # Exp 7: Relational Joins & Set Operations
│   ├── 08_views_and_triggers.txt               # Exp 8: View Abstraction & Change-Log Triggers
│   └── 09_transactions_and_concurrency.txt    # Exp 9: ACID Transactions & Concurrency Locking
│
└── 04_Student_College_Basic/       # Beginner-friendly MySQL Workbench edition
    ├── 01_database_creation.txt                # Exp 1: Student-College Database (Basic Setup)
    ├── 02_er_to_relational_mapping.txt         # Exp 2: ER/EER to Relational Schema
    ├── 03_ddl_and_integrity_constraints.txt   # Exp 3: DDL & Constraints
    ├── 04_dml_insert_update_delete.txt         # Exp 4: DML (Insert, Update, Delete)
    ├── 05_dcl_grant_and_revoke.txt            # Exp 5: DCL (Grant and Revoke)
    ├── 06_queries_and_aggregate_functions.txt  # Exp 6: Basic Select & Aggregate Functions
    ├── 07_join_operations.txt                 # Exp 7: Join Operations
    ├── 08_views_and_triggers.txt               # Exp 8: Views & Triggers
    └── 09_transactions_and_concurrency.txt    # Exp 9: Transaction & Concurrency Control
```

---

## 🚀 How to Execute in MySQL / MySQL Workbench

1. **Launch MySQL Client or Workbench**:
   ```bash
   mysql -u root -p
   ```
2. **Execute an experiment file**:
   Open any `.txt` file from the repository, copy the SQL commands, or execute via CLI:
   ```bash
   mysql -u root -p < DBMS/01_Easy_Separate_Examples/01_database_creation.txt
   ```
3. **Verify engine support**:
   For Experiment 9 (Transactions and Row Locking), ensure your database engine is **InnoDB** (`ENGINE = InnoDB`) so that `START TRANSACTION`, `COMMIT`, `ROLLBACK`, and `FOR UPDATE` locks operate with full ACID guarantees.

---

## 📚 Experiment Overview Matrix

| # | File Name | Operation / Key SQL Concepts | Primary Tables |
|---|---|---|---|
| **1** | `01_database_creation.txt` | `CREATE DATABASE`, `CREATE TABLE`, `PRIMARY KEY`, `NOT NULL`, `INSERT INTO`, `SELECT` | `department`, `student`, `course`, `book` |
| **2** | `02_er_to_relational_mapping.txt` | Entity translation, M:N relationship decomposition, Composite Primary Keys | `member`, `borrow`, `enrollment` |
| **3** | `03_ddl_and_integrity_constraints.txt` | `ALTER TABLE ADD/MODIFY/DROP`, `CHECK`, `UNIQUE`, `DEFAULT`, `RENAME`, `TRUNCATE`, `DROP` | `product`, `customer`, `test_item` |
| **4** | `04_dml_insert_update_delete.txt` | Conditional `UPDATE`, `DELETE WHERE`, `INSERT INTO ... VALUES` | `account`, `student` |
| **5** | `05_dcl_grant_and_revoke.txt` | `CREATE USER`, `GRANT SELECT, INSERT`, `REVOKE`, `SHOW GRANTS` | `teacher`, `student` |
| **6** | `06_queries_and_aggregate_functions.txt` | `WHERE`, `AND`, `OR`, `BETWEEN`, `IN`, `LIKE`, `ORDER BY`, `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`, `GROUP BY`, `HAVING` | `employee`, `student` |
| **7** | `07_join_operations.txt` | `INNER JOIN`, Non-Equijoin (`> / <`), `SELF JOIN`, `LEFT OUTER JOIN`, `RIGHT OUTER JOIN`, `CROSS JOIN` | `customer`, `orders`, `department` |
| **8** | `08_views_and_triggers.txt` | `CREATE VIEW`, `DELIMITER //`, `AFTER INSERT`, `AFTER UPDATE`, `AFTER DELETE`, audit table logging | `product_log`, `student_log`, `view` |
| **9** | `09_transactions_and_concurrency.txt` | `START TRANSACTION`, `COMMIT`, `ROLLBACK`, `SELECT ... FOR UPDATE` (Pessimistic Row Lock) | `wallet`, `student` |
