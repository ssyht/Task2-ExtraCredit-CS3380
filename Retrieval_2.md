## Retrieval Task 2

**English Description**

**Task 2:**
For each fruit form (Fresh, Canned, Juice, Dried, Frozen), find the average retail price and list the form together with that average price.

```sql
SELECT
    Form,
    AVG(RetailPrice) AS AvgRetailPrice
FROM Fruit_Prices_2022
GROUP BY Form;
```

### Is this SQL query correct?**

Yes, this query is correct.

### Reasoning:

GROUP BY Form groups all rows by the fruit form (Fresh, Canned, Juice, Dried, Frozen, etc.).

AVG(RetailPrice) computes the average retail price within each form group.

The query returns one row per Form with that form’s average price (AvgRetailPrice), which matches the English description.

Only aggregated columns and the grouped column (Form) are in the SELECT list, so the SQL is valid.
