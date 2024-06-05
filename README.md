# Module 22 Challenge
# Home Sales Analysis with SparkSQL

## Overview
This project utilizes PySpark and SparkSQL to analyze a home sales dataset. The main objectives are to determine key metrics about home sales, create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

## Files
- `Home_Sales_Colab.ipynb`: The Google Collaboratory Notebook containing the complete analysis and code.

## Setup Instructions
1. Clone the repository to your local machine
2. Open Home_Sales_Collab.ipynb using Google Colab.
3.Ensure you have the necessary packages installed.
4. Run the notebook cells to execute the analysis.

# Analysis Steps
## Data Loading: The dataset is loaded into a Spark DataFrame from a CSV file.
Temporary Table Creation: A temporary table called home_sales is created from the DataFrame.

## Queries:
1) Average Price for Four-Bedroom Houses: The average price for four-bedroom houses sold each year.
2) Average Price for Homes with Specific Features: The average price of homes built each year with three bedrooms and three bathrooms.
3) Average Price for Larger Homes with Specific Features: The average price of homes with three bedrooms, three bathrooms, two floors, and at least 2,000 square feet.
4) Average Price per "View" Rating: The average price of a home per "view" rating for homes with an average price greater than or equal to $350,000.

## Caching and Uncaching:
The temporary table home_sales is cached to improve query performance.
The same query on average price per "view" rating is executed on the cached table to compare runtime.

## Partitioning:
The dataset is partitioned by the date_built field and saved as a Parquet file.
A temporary table for the Parquet data is created.
The query on average price per "view" rating is run on the partitioned data to compare runtime.

## Validation:
The home_sales temporary table is uncached and verified to be uncached.


# Summary
This project demonstrates the power and efficiency of using PySpark and SparkSQL for big data analysis. By creating temporary views, partitioning data, and utilizing caching, we were able to significantly improve query performance. The analysis provided key insights into the home sales dataset, such as the average prices for homes with specific features and the impact of "view" ratings on home prices. This project highlights the importance of optimizing data processing techniques to handle large datasets effectively.

