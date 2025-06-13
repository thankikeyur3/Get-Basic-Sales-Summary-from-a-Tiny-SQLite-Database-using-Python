# Get-Basic-Sales-Summary-from-a-Tiny-SQLite-Database-using-Python


# 🧮 Task 7: Sales Summary using SQLite and Python

## 🎯 Objective
The goal of this task is to use Python with SQLite to generate a basic sales summary report and visualize the results using a bar chart.

---

## 🛠 Tools Used
- Python
- SQLite3 (built-in)
- pandas
- matplotlib

---

## 🗂️ Dataset
A sample SQLite database (`sales_data.db`) was created with a single table named `sales`.  
Sample data includes product names, quantity sold, and price.

---

## 🧾 Steps Performed

1. **Created SQLite database**: `sales_data.db` with a `sales` table.
2. **Inserted sample sales records** into the table.
3. **Connected Python to SQLite** using `sqlite3`.
4. **Executed SQL query** to calculate:
   - Total quantity sold per product
   - Total revenue per product
5. **Loaded query result into pandas** for processing.
6. **Displayed output using `print()`**.
7. **Plotted a bar chart** using matplotlib showing revenue by product.
8. **Saved the chart** as `sales_chart.png`.

---

## 📊 SQL Query Used
```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
```

---

## 🖼 Output

- Console table output using pandas.
- Bar chart: `sales_chart.png` (revenue by product)
