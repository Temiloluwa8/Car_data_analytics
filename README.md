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

## Data Overview
The dataset includes the following columns:
>+ Dealer Information – Names, regions, and performance of car dealers.
>+ Car Details – Models, body styles, transmission types, and prices.
>+ Sales Data – Number of cars sold, revenue generated, and average sale prices.
>+ Customer Demographics – Gender and income levels of buyers.
>+ Time-Based Data – Sales trends by months or years for performance tracking.

## Data Visualization
[To view the powerbi dashboard, click here](https://ibb.co/0VFGRtk7)

## SQL
```sql
SELECT * FROM car_dataset;
```

```sql
SELECT DISTINCT model 
FROM car_dataset;
```

```sql
SELECT COUNT(*) AS Total_Cars_Sold 
FROM car_dataset;
```

```sql
SELECT * FROM car_dataset
WHERE Dealer_Name = "Buddy Storbeck's Diesel Service Inc";
```

```sql
SELECT * FROM car_dataset 
  WHERE Date = '01/02/2022';
```
