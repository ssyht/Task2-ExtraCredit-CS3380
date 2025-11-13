# CS 3380 – Task 2 (Extra Credit)  
SQL Retrieval Tasks on Fruit Prices Data

This repository contains my solution for the CS 3380 extra credit assignment using the **Fruit-Prices-2022** dataset. The goal is to design three English retrieval tasks and write SQL queries that correctly answer each task, plus explain whether each query is correct and why.

---

## Dataset

**File:** `Fruit-Prices-2022.csv`

Assumed table name in SQL examples: **`Fruit_Prices_2022`**

Assumed columns:

- `Fruit`
- `Form`
- `RetailPrice`
- `RetailPriceUnit`
- `Yield`
- `CupEquivalentSize`
- `CupEquivalentUnit`
- `CupEquivalentPrice`

> Note: If your actual table or column names differ, adjust the SQL accordingly.

---

## Retrieval Task 1

### English Description

> **Task 1:**  
> List all fresh fruits that cost less than \$2.00 per pound, showing the fruit name, retail price, yield, and retail price unit, ordered from the cheapest to the most expensive.

### SQL Query

```sql
SELECT
    Fruit,
    Form,
    RetailPrice,
    RetailPriceUnit,
    Yield
FROM Fruit_Prices_2022
WHERE Form = 'Fresh'
  AND RetailPriceUnit = 'per pound'
  AND RetailPrice < 2.00
ORDER BY RetailPrice ASC;
