# Accord Hardware -Sales-Analysis
Sales Insights Data Analysis Project
# setup mysql on  local computer
1. Configure  mysql on local computer 
2. SQL database dump is in Rakeshdumb.sql file in import in my sql database
# Setup Tableau Desktop on  computer

#Data Analysis Using SQL
1. Show all customer records

SELECT * FROM customers;

2. Show total number of customers

SELECT count(*) FROM customers;

3. Show transactions for Delhi NCR market (market code for Delhi NCR is Mark004)

SELECT * FROM transactions where market_code='Mark004';

4. Show distrinct product codes that were sold in Mumbai

SELECT distinct product_code FROM transactions where market_code='Mark002';

5. Show transactions where currency is US dollars

SELECT * from transactions where currency="USD"

6.Show transactions in 2020 join by date table

SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

7. Show total revenue in year 2020,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

8. Show total revenue in year 2020, January Month,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

9.Show total revenue in year 2020 in Bhopal

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark007";
