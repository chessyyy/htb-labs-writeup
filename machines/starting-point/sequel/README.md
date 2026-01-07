# HTB – Sequel

**Difficulty:** Very Easy  
**Category:** Database / MySQL  
**OS:** Linux  

---

## Overview

Sequel is a Hack The Box Starting Point machine designed to introduce basic database enumeration and interaction using MySQL/MariaDB. The lab focuses on identifying exposed database services and interacting with them using standard command-line tooling.

This machine highlights the risks associated with insecure database configurations, such as allowing privileged access without authentication.

---

## Assessment Tasks & Answers (Non-Flag)

The following assessment tasks were completed as part of the HTB Sequel lab. These questions validate understanding of fundamental database concepts and enumeration techniques. Flag values are intentionally excluded.

---

### Task 1: Database Service Enumeration

**Question:**  
During enumeration, which port is found serving MySQL?

**Hint:**  
The answer is under the PORT column of the nmap scan of our target host.

**Answer:**  
3306

---

### Task 2: Database Engine Identification

**Question:**  
What community-developed MySQL-compatible database engine is the target running?

**Hint:**  
Typically '-sV' is used with Nmap to determine versions, but that's not always enough. In this case, try adding '-sC' to run safe scripts, which is another good way to get things like versions.

**Answer:**  
MariaDB

---

### Task 3: MySQL Client Usage

**Question:**  
When using the MySQL command-line client, what switch is used to specify a login username?

**Hint:**  
The answer can be found in MySQL's help menu.

**Answer:**  
-u

---

### Task 4: Authentication Weakness

**Question:**  
Which username allows access to the MariaDB instance without providing a password?

**Hint:**  
The root of all evil.

**Answer:**  
root

---

### Task 5: SQL Query Syntax

**Question:**  
In SQL, what symbol is used to select all columns from a table?

**Hint:**  
This will make you starry-eyed.

**Answer:**  
*

---

### Task 6: SQL Statement Termination

**Question:**  
In SQL, what symbol is required to terminate each query?

**Hint:**  
You can find the answer by reading the write-up carefully.

**Answer:**  
;

---

### Task 7: Database Enumeration

**Question:**  
Three databases are commonly present in all MySQL installations. What is the name of the fourth database that is unique to this host?

**Hint:**  
Try 'show databases;' to list the databases, and then read about default databases in the MySQL documentation.

**Answer:**  
htb

---

> **Note:** Root flags, credentials, and sensitive exploitation details are intentionally excluded in accordance with Hack The Box content guidelines.
