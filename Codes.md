 #Codes

 ```sql

select * from smartphone;
select * from dimension;

# Check for missing values in Dimentional table,
SELECT * FROM dimension WHERE price is NULL OR avg_rating IS NULL;
SELECT * FROM dimension WHERE battery_capacity is NULL OR num_cores IS NULL;
SELECT * FROM dimension WHERE processor_speed is NULL OR fast_charging_available IS NULL;
SELECT * FROM dimension WHERE ram_capacity is NULL OR internal_memory IS NULL;

# check for missing values in Fact table,
select * from smartphone where processor_brand is null or os is null;

# Aggregation Operation (GROUP BY)
SELECT avg_rating, AVG(price) AS avg_price
FROM dimension
GROUP BY avg_rating;

SELECT ram_capacity, AVG(price) AS avg_price
FROM dimension
GROUP BY ram_capacity;

# Join Operation
SELECT s.ï»¿brand_name, avg(d.price) as avg_price
FROM smartphone s
JOIN dimension d ON s.model = d.model
GROUP BY s.ï»¿brand_name; 

SELECT * FROM dimension JOIN smartphone ON dimension . model = smartphone . model;  

```
