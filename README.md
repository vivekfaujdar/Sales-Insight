Project Description:

The project shows the sales insights of the ATLIQ HARDWARE in INDIA which sells millions of products each year. To track down the live sales and revenue/cost, I generated a POWER BI based report along with the dashboard to check what sales have patterns throughout the years and months.

Procedure:
1. Use of AIMS grid to define purpose and planning.
2. Import data into MySQL, and plug MySQL database with Power BI
3. Performed data cleaning and ETL (Extract, Transform, Load).
4. Success in building Automated Dashboard to provide latest sales insights to support data driven decision making. Sales team able to take batter decision and saving    10% cost of total spending and 20% of business time.

Tools Used:
   1. MYSQL Workbench
   2. Microsoft Power BI Desktop
 
 Some Queries that helped me in the project:
 1. Show transactions in 2020 join by date table:
 
        SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

 2. Show total revenue in year 2020:
      
        SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";
      
3. Show total revenue in year 2020, January Month:

        SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");
        
4. Show total revenue in year 2020 in Chennai:

        SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";
