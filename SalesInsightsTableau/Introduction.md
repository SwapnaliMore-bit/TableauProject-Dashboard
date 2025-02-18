## Sales Insights Data Analysis Project:
 An automated dashboard providing quick & latest sales insights in order to support data-driven decision-making.

## Purpose : 
 To unlock sales insights that are not visible before for the sales team for decision support and automate them to reduce manual time spent on data furthering.

## Result :  
 An automated dashboard providing quick and latest sales insights in order to support data-driven decision-making.
   

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

2. Show total number of customers

    `SELECT count(*) FROM customers;`

3. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

4. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

5. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

6. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

7. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
8. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and 		 
      date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

9. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
	and transactions.market_code="Mark001";`
10. total Revenue
    
 	`select sum(sales_amount) from transactions;`

12. total sales quantity
    
	`select sum(sales_qty) from transactions;`

12. Revenue by market

 `select sum(transactions.sales_amount),markets.markets_name from transactions inner join markets
 on transactions.market_code=markets.markets_code group by markets.markets_name
 order by sum(transactions.sales_amount) desc;`
 
 13. sales_quanlity by markets
     
 `select sum(transactions.sales_qty),markets.markets_name from transactions inner join markets
 on transactions.market_code=markets.markets_code group by markets.markets_name
 order by sum(transactions.sales_qty) desc;`
  
  

