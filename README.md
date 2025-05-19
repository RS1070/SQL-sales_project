# 🛍️ Retail Sales Data Analysis (SQL Project)

This project presents an end-to-end analysis of retail sales data using SQL. It involves data cleaning, exploration, and the answering of 10 real-world business questions on sales performance, customer behavior, and product category trends.

---

## 📁 Project Files

- `sqlproject1.sql`: Contains all SQL queries used in this project—data cleaning, exploration, and analysis.
- `SQL - Retail Sales Analysis_utf .csv`: The source dataset containing retail transaction data.

---

## 📊 Dataset Description

The dataset contains transactional data with the following key fields:
- `transactions_id`: Unique transaction identifier
- `sale_date`, `sale_time`: Timestamp of the sale
- `customer_id`: Unique identifier for each customer
- `gender`, `age`: Demographics of the customer
- `category`: Product category (e.g., Clothing, Beauty, etc.)
- `quantiy`: Quantity purchased (note the typo in original column name)
- `cogs`, `total_sale`: Cost of goods sold and final sale amount

---

## 🧹 Data Cleaning

The dataset is cleaned by removing any rows where key columns are `NULL`, including:
- `transactions_id`, `sale_date`, `sale_time`, `gender`, `category`, `quantiy`, `cogs`, `total_sale`

```sql
DELETE FROM retail_sales
WHERE transactions_id IS NULL OR sale_date IS NULL ...
```

---

## 🔍 Key Business Questions Answered

1. **Sales on a specific date**: Filter transactions for 5th Nov 2022.
2. **High volume Clothing sales in Nov 2022**.
3. **Total sales per category**.
4. **Average customer age for Beauty category**.
5. **Transactions with total sale > 1000**.
6. **Gender-wise transactions by category**.
7. **Best selling month each year (based on average sales)**.
8. **Top 5 customers by total sales**.
9. **Unique customers per category**.
10. **Shift-wise (Morning, Afternoon, Evening) transaction volumes**.

---

## 🛠️ Technologies Used

- PostgreSQL (compatible with any SQL RDBMS)
- SQL window functions, aggregations, CTEs
- Data exported/imported from `.csv` for testing

---

## 📌 Insights & Learnings

- Use of `RANK()` and `EXTRACT()` to identify top-performing months
- Shift analysis based on transaction hour using `CASE WHEN`
- Effective cleaning pipeline to remove incomplete records
- Business-oriented querying to support decision-making

---

## ✅ How to Use

1. Load the CSV into a SQL table named `retail_sales`.
2. Run `sqlproject1.sql` file step-by-step.
3. Modify queries as needed to tailor to your database.

---

## 📎 License

This project is open for educational and non-commercial use. Please credit the repository if reused or referenced.

---

## 📬 Contact

For any queries, suggestions, or collaborations:  
📧 Rajats2901@gmail.com  
🔗 [LinkedIn: Rajat Singh](https://www.linkedin.com/in/rajat-singh-258b22250/)