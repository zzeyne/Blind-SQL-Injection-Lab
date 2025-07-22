# Blind-SQL-Injection-Lab
Educational lab on Blind(Time Based) SQL Injection attacks using login forms and URL manipulation
# Time-Based Blind SQL Injection Demo

This project demonstrates a basic **time-based blind SQL injection** attack by exploiting a vulnerable URL parameter.

## 🛠 What I Did

### 1. Time Delay via Conditional Injection

- I targeted a web application with a vulnerable URL parameter (e.g., `id=1`).
- I injected SQL payloads with **conditional time delays**.
- If the condition I wrote was **true**, the server delayed the response by **10 seconds** using SQL functions like `SLEEP(10)`.

**Example Payload:**

```sql
id=1' AND IF(1=1, SLEEP(10), 0)-- -
