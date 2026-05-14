# retail-sales-analytics-project
Day-01/
CREATE TABLE sales (
    order_id INT PRIMARY KEY,
    customer_name VARCHAR(50),
    product VARCHAR(50),
    category VARCHAR(50),
    region VARCHAR(50),
    sales_amount INT,
    order_date DATE
);
INSERT INTO sales VALUES
(1,'John','Laptop','Electronics','East',1200,'2026-05-01'),
(2,'Sara','Phone','Electronics','West',800,'2026-05-02'),
(3,'Mike','Chair','Furniture','South',300,'2026-05-03'),
(4,'Emma','Desk','Furniture','North',450,'2026-05-04'),
(5,'David','Tablet','Electronics','East',600,'2026-05-05');
select * from sales;
select SUM(sales_amount)as Total_sales from sales;
select region,sum(sales_amount) from sales
group by region;
select category,sum(sales_amount)
from sales 
group by category
order by sum(sales_amount) desc;
select product,sales_amount 
from sales 
order by sales_amount desc;
select * from sales
order by sales_amount
limit 1;
Day-01/
