# Task 7: Creating Views

## Objective:
To understand and practice the creation and use of SQL Views for data abstraction and reusability.

## What I Did:
- Created SQL views using `CREATE VIEW`.
- Used SELECT queries on the views.
- Explored view benefits such as simplification and security.

## Tools Used:
- MySQL Workbench 

## Example Code:
```sql
-- Creating a view for top selling products
CREATE VIEW top_products AS
SELECT product_name, SUM(quantity) AS total_sold
FROM sales
GROUP BY product_name
HAVING total_sold > 100;

-- Using the view
SELECT * FROM top_products;
