# Car_Sale_Analytics
This is a car sales performance report by dealers, models, and customers

---
## Car_Sale_Report
_The report provide key insights into sales performance, customer demographics, revenue trends, and vehicle preferences_

---
## Project Overview
> This project provides a comprehensive analysis of car sales data. It highlights key metrics such as total revenue, total cars sold, average sales price, and customer count. Users can explore sales performance across different dealers, car models, and regions. The report also includes insights into customer demographics and vehicle preferences. Interactive visuals and filters make it easy to drill down and uncover trends for better decision-making

## Data Source:
+ www.kaggle.com

## Tools Used
### Power BI used for: 
      1. Data Visualization – Created clear and interactive visuals to display key car sales metrics.
      2. Data Modeling & DAX – Built relationships and calculated insights using DAX formulas.
      3. Interactive Reporting – Enabled filters and slicers for dynamic data exploration.
### Excel used for :
      1. Pivot Tables – Summarized large datasets to analyze sales by dealer, region, and model.
      2. Charts & Graphs – Visualized trends, comparisons, and key metrics like monthly sales and customer breakdown.
      3. Formulas & Functions – Used Excel functions to calculate totals, averages, and filter data dynamically.

## Data Overview
The dataset includes the following columns:
>+ Dealer Information – Names, regions, and performance of car dealers.
>+ Car Details – Models, body styles, transmission types, and prices.
>+ Sales Data – Number of cars sold, revenue generated, and average sale prices.
>+ Customer Demographics – Gender and income levels of buyers.
>+ Time-Based Data – Sales trends by months or years for performance tracking.

## Data Visualization
[To view the powerbi dashboard, click here](https://ibb.co/0VFGRtk7)

[To view the excel dashboard, click here](https://ibb.co/9kjnn03P)

## Dashboard Visuals

![CAR SALES POWER BI DASHBOARD](https://github.com/user-attachments/assets/ec5bc5c9-9ddd-4af5-99fa-17cb7d6584fb)

![CAR SALES ANALYSIS EXCEL DASHBOARD](https://github.com/user-attachments/assets/de93f49e-99e3-4f53-b11c-6f1ec96d334e)


## SQL
```sql
## Retrieving all data from table
SELECT *
FROM car_dataset;
```

```sql
## To get all unique car models sold
SELECT DISTINCT model 
FROM car_dataset;
```

```sql
## Finding the total number of cars sold
SELECT COUNT(*)
AS Total_Cars_Sold 
FROM car_dataset;
```

```sql
## To get all sales made by a specific dealer (e.g., "Buddy Storbeck's Diesel Service Inc")
SELECT *
FROM car_dataset
WHERE Dealer_Name = "Buddy Storbeck's Diesel Service Inc";
```

```sql
## Retrieving all sales from a specific date (e.g., '2024-01-15')
SELECT *
FROM car_dataset 
WHERE Date = '01/02/2022';
```

```sql
## Finding the total revenue generated from car sales
SELECT SUM(`Price ($)`)
AS Total_Revenue
FROM car_dataset;
```

```sql
## Counting the number of cars sold by each dealer
SELECT Dealer_Name, COUNT(*) AS Cars_Sold 
FROM car_dataset 
GROUP BY Dealer_Name
ORDER BY Cars_Sold DESC;
```

```sql
## To get the average car price per company
SELECT Company, round(AVG(`Price ($)`),2) AS Avg_Car_Price 
FROM car_dataset 
GROUP BY Company
ORDER BY Avg_Car_Price DESC;
```

```sql
## Retrieving the most expensive car sold
SELECT *
FROM car_dataset 
ORDER BY (`Price ($)`) DESC LIMIT 1;
```

```sql
## Retrieving sales data where the customer has an annual income greater than $100,000
SELECT *
FROM car_dataset 
WHERE `Annual Income` > 100000;
```

```sql
## To get the number of cars sold by body style
SELECT `Body Style`, COUNT(*) AS Cars_Sold 
FROM car_dataset 
GROUP BY `Body Style`
ORDER BY Cars_Sold DESC;
```

```sql
## Retrieving the number of male and female customers who bought cars
SELECT Gender, COUNT(*) AS Customer_Count 
FROM car_dataset
GROUP BY Gender;
```

```sql
## Finding the top 5 most sold car models
SELECT Model, COUNT(*) AS Cars_Sold 
FROM car_dataset 
GROUP BY Model
ORDER BY Cars_Sold DESC LIMIT 5;
```

```sql
## Finding the least expensive car sold
SELECT *
FROM car_dataset 
ORDER BY `Price ($)` ASC LIMIT 1;
```

```sql
## Retrieving all sales for cars of a specific color (e.g., 'White')
SELECT *
FROM car_dataset 
WHERE LOWER(Color) = 'black';
```
