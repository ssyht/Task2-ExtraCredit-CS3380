Retrieval Task 3
English Description

## Task 3:

**Find the fruit (name and form) that has the highest cup-equivalent price in the dataset, and show its fruit name, form, cup-equivalent price, and cup-equivalent unit.**

```sql
SELECT
    Fruit,
    Form,
    CupEquivalentPrice,
    CupEquivalentUnit
FROM Fruit_Prices_2022
ORDER BY CupEquivalentPrice DESC
LIMIT 1;
```
**Is this SQL query correct?**

Yes, this query is correct.

**Reasoning:**

``ORDER BY CupEquivalentPrice DESC`` sorts the entire table by cup-equivalent price from highest to lowest.

``LIMIT 1`` returns only the single row with the highest CupEquivalentPrice.

The selected columns (``Fruit, Form, CupEquivalentPrice, CupEquivalentUnit``) match exactly what the task asks us to show:

``fruit name``

``form``

``cup-equivalent price``

``cup-equivalent unit``

Therefore, this query directly answers the question: it returns the fruit and form with the highest cup-equivalent price, along with the requested details.
