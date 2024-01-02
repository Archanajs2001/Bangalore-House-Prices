# Power BI Project: Bangalore House Prices

## Overview

Welcome to the Bangalore House Prices Power BI project! This project focuses on analyzing and visualizing housing prices in Bangalore based on a dataset containing details about housing units. The data covers various aspects such as size, location, total square footage, and prices. The visualizations and insights aim to provide a comprehensive view of the housing market in Bangalore.

 
## Table of Contents

- [Data Cleaning](#data-cleaning)
- [Data Transformation in Power BI](#data-transformation-in-power-bi)
- [Visualizations](#visualizations)
- [Slicers](#slicers)
- [Instructions](#instructions)


## Data Cleaning

Data cleaning was performed in Google Colab using Python. The process included handling null values, making adjustments to columns like 'total_sqft.' and 'size'. Separate datasets were created by filtering the top 4 sizes (e.g., 1 BHK, 2 BHK, 3 BHK, 4 BHK). This allows for focused analysis on the most sought-after housing unit sizes.The code for data cleaning is available in the repository.


## Data Transformation in Power BI

- **Added Column: 'Price/Sq.Ft.'**
  - Calculated using DAX language to provide a metric for price efficiency.
    ```DAX
    price/sqft = DIVIDE('cleaned data'[price], 'cleaned data'[total_sqft])
    ```
- **New Measure: 'Total Housing Units'**
  - Computed using DAX to offer a dynamic measure for the total housing units based on applied filters.
    ```DAX
    total available houses = COUNTROWS('cleaned data')
    ```


## Visualizations

- **Total Housing Units (Card):**
  - Overview of the total number of housing units in Bangalore using card.
  
- **Housing Units by Area Type (Pie Chart):**
  - Distribution of housing units based on area type using pie chart.

- **Housing Units by Size (Bar Chart):**
  - Breakdown of housing units by size using bar chart.

- **Housing Units by Location and Size (Stacked Bar Chart):**
  - Visual representation of housing units categorized by location and size using stacked bar chart.

- **Average Price by Location for 1, 2, 3, and 4 BHK (Area Chart):**
  - Trends in average prices for 1, 2, 3, and 4 BHK units, highlighting the most sought-after sizes using area chart.

- **Location, Total Sqft., Price, and Price per Sqft. (Table):**
  - Detailed table presenting key information for analysis.


## Slicers

The report includes three slicers for enhanced interactivity:

- **Size Slicer:**
  - Filter the report by housing unit size (e.g., 1 BHK, 2 BHK).

- **Location Slicer:**
  - Narrow down the analysis based on the housing unit's location in Bangalore.

- **Bath Slicer:**
  - Further refine the insights by selecting the number of bathrooms in the housing units.


## Instructions

1. Open the Power BI file in Power BI Desktop.
2. Ensure that the necessary data connections are established.
3. Explore the visualizations and insights in the report page.
4. Utilize slicers for interactive filtering based on size, location, and bath.
5. Refer to the documentation for details on data sources, transformations, and visualizations.

This Power BI project provides a comprehensive overview of Bangalore house prices, enabling users to gain valuable insights into the housing market in the region.

Feel free to reach out for any questions or feedback! Enjoy exploring the fascinating world of Bangalore house prices.






