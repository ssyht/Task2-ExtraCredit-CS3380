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
