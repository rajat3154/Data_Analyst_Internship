# TASK-6-Sales-Trend-Analysis-Using-Aggregations



# Sales Trend Analysis Using MySQL

## 📊 Objective
Analyze monthly revenue and order volume from an e-commerce sales dataset using MySQL.

---

## 🧰 Tools & Technologies
- MySQL Workbench
- SQL
- CSV Import Wizard
- Table Creation and Data Insertion
- SQL Aggregation Functions

---

## 📁 Dataset
The dataset was derived from [Keith Galli's Pandas Data Science Tasks]  
It includes fields like `Order ID`, `Product`, `Quantity Ordered`, `Price Each`, `Order Date`, `Purchase Address`, and more.

---

## 🛠️ Steps Performed

1. **Table Creation**

```sql
CREATE TABLE sales (
    order_id VARCHAR(20),
    product VARCHAR(100),
    quantity_ordered INT,
    price_each DECIMAL(10,2),
    order_date DATETIME,
    purchase_address VARCHAR(255)
);
```

2. **Imported 100 Sample Entries**  
Generated and inserted 100 mock sales records using SQL `INSERT` statements.

3. **Added Derived Columns**

```sql
ALTER TABLE sales 
ADD COLUMN month INT, 
ADD COLUMN hour INT, 
ADD COLUMN sales DECIMAL(10,2), 
ADD COLUMN city VARCHAR(100);
```

4. **Populated Derived Columns**

```sql
UPDATE sales
SET 
    month = MONTH(order_date),
    hour = HOUR(order_date),
    sales = quantity_ordered * price_each,
    city = SUBSTRING_INDEX(SUBSTRING_INDEX(purchase_address, ',', -2), ',', 1);
```

5. **Performed Aggregation for Monthly Sales and Orders**

```sql
SELECT
    YEAR(order_date) AS year,
    MONTH(order_date) AS month,
    SUM(sales) AS total_revenue,
    COUNT(DISTINCT order_id) AS total_orders
FROM
    sales
GROUP BY
    YEAR(order_date), MONTH(order_date)
ORDER BY
    YEAR(order_date), MONTH(order_date);
```

---

## 📈 Results Table

| year | month | total_revenue | total_orders |
|------|--------|----------------|---------------|
| 2024 | 1      | 83151.57       | 25            |
| 2024 | 2      | 96935.81       | 28            |
| 2024 | 3      | 85887.61       | 21            |
| 2024 | 4      | 54555.15       | 26            |

---

## ✅ Outcome

We successfully analyzed the monthly sales trend and order volume using SQL aggregations on structured e-commerce sales data. This helped in identifying monthly revenue patterns and sales performance.

