# Pizza Sales Analysis (SQL)

SQL analysis of one year of pizza sales data (2015) to find out what sells, when it sells and how much revenue it brings in. Queries were written and run in **MySQL Workbench**, and the findings are presented in a PowerPoint deck.

## Business Questions

**Basic**
- Total number of orders placed
- Total revenue generated from pizza sales
- Highest-priced pizza
- Most common pizza size ordered
- Top 5 most ordered pizza types with quantities

**Intermediate**
- Total quantity of each pizza category ordered
- Distribution of orders by hour of the day
- Category-wise distribution of pizzas
- Average number of pizzas ordered per day
- Top 3 most ordered pizza types by revenue

**Advanced**
- Percentage contribution to total revenue
- Cumulative revenue over time
- Top 3 pizza types by revenue within each category

## Dataset

Four related tables:

| Table | Purpose |
|---|---|
| `orders` | order_id, order date, order time |
| `orders_details` | order_details_id, order_id, pizza_id, quantity |
| `pizzas` | pizza_id, pizza_type_id, size, price |
| `pizza_types` | pizza_type_id, name, category, ingredients |

## Key Findings

| Metric | Result |
|---|---|
| Total orders | 21,350 |
| Total revenue | $817,860.05 |
| Highest-priced pizza | The Greek Pizza ($35.95) |
| Most common size | L (18,526 order lines) |
| Average pizzas per day | 138 |
| Best-selling pizza | The Classic Deluxe Pizza (2,453 units) |
| Top revenue pizza | The Thai Chicken Pizza ($43,434.25) |
| Top category by quantity | Classic (14,888) |
| Peak order hours | 12:00 and 13:00, then 17:00 |

Revenue share by category: Classic 26.91%, Supreme 25.46%, Chicken 23.96%, Veggie 23.68%.

## SQL Skills Demonstrated

- **Data retrieval:** `SELECT`, `WHERE`, `ORDER BY`, `LIMIT`
- **Aggregation:** `COUNT()`, `SUM()`, `AVG()`, `ROUND()`, `GROUP BY`
- **Joins:** multi-table `INNER JOIN` across 3-4 tables
- **Subqueries:** nested queries and derived tables
- **Window functions:** `SUM() OVER (ORDER BY ...)` for cumulative revenue, `RANK() OVER (PARTITION BY ...)` for ranking within categories
- **Date and time functions:** `HOUR()` for hourly order distribution
- **Calculated fields:** revenue = quantity x price, percentage of total revenue

## Tools

- MySQL / MySQL Workbench
- Microsoft PowerPoint (report)

## Repository Structure

```
pizza-sales-sql-analysis/
├── README.md
├── pizza_sales_queries.sql
├── Pizza_sales_Pdf.pdf
└── data/            (optional: CSV files for the four tables)
```

## Author

Shakeel Nawaz Khan
