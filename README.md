# Financial Assets Performance Overview Dashboard

This project analyzes the performance of various financial assets over time, using statistical methods and visualizations to extract key insights on asset price trends, trade volumes, and security composition.

## Project Overview

![image](https://github.com/user-attachments/assets/91836ff8-12d4-4ce0-aa43-b361de4736a2)


I used historical stock data from various security groups, including Stocks, Cryptocurrency, Indices, Metals, and Energy. The main goal is to analyze price trends, trade volumes, and market performance for each category.

### Key Objectives:
1. **Analyze price trends** across different security groups over time.
2. **Examine trade volumes** and identify dominant securities.
3. **Create visualizations** to represent asset performance.

## Data Used

The dataset used for this analysis consists of five main fields:
- **Date**: The date on which the data point was recorded.
- **Security**: Specific assets or stocks.
- **Security Group**: Category to which each security belongs (e.g., Stocks, Cryptocurrency, Metals).
- **Price**: Price of the security.
- **Volume**: Volume of trades for the respective security.

The data spans from 2020 to 2024 and captures fluctuations in prices and volumes over time.

## Analysis Methods

### 1. **Statistical Summary**:
   I started with a basic summary of the data by calculating the mean prices and median traded volumes for each security group.

   - **Python Functions Used**:
     - `groupby()` to group data by security group.
     - `agg()` to compute summary statistics.
     - `mean()` for calculating average prices.
     - `median()` to compute median volumes.

   - **Summary Findings**:
     - **Average Price per Security Group**:
       - Cryptocurrency: \$15,473.69
       - Energy: \$36.79
       - Indices: \$8,501.07
       - Metals: \$711.02
       - Stocks: \$47,403.12
     - **Median Volume of Trades**:
       - Cryptocurrency: 473,760 units
       - Energy: 190,050 units
       - Indices: 223,950,000 units
       - Metals: 57,610 units
       - Stocks: 29,440,000 units

     These numbers highlight how Stocks and Cryptocurrencies have higher prices and volumes compared to more stable categories like Energy and Metals.

### 2. **Price Trends Analysis**:
   I used a pivot table to examine the price trends over time for each security group.

   - **Python Functions Used**:
     - `pivot_table()` to reshape data and analyze prices across time.
     - `aggfunc='mean'` to compute average prices for each date.

   - **Summary of Price Trends**:
     - **Cryptocurrency**: Grew significantly from \$3,500 in early 2020 to much higher prices by 2024.
     - **Energy**: Showed relative stability, with prices around \$30-32.
     - **Indices and Metals**: Stable with slight fluctuations.
     - **Stocks**: Consistently high prices with upward trends over time.

### 3. **Dashboard Visualization**:
   I made a dashboard in Tableau to visualize:
   - **Proportion of Volume Traded**: Highlighting that **Indices** and **Stocks** dominated the market in terms of trade volumes.
   - **Average Price Trend**: Showing consistent upward trends in **Stocks** and **Cryptocurrencies**.
   - **Price Trend for Each Segment**: Illustrating how **Cryptocurrencies** and **Indices** experience more volatility compared to stable asset groups like **Metals**.

## Tools & Techniques Used

- **Python**:
  - Data cleaning, aggregation, and statistical analysis were done using Python libraries:
    - `pandas` for data manipulation.
    - `numpy` for numerical computations.
    - `matplotlib` and `seaborn` (optional) for visualizing trends during exploratory analysis.
  
- **Tableau**:
  - Used for creating interactive visualizations that depict:
    - Proportions of traded volumes.
    - Price trends across time.
    - Securities composition and average prices.

- **Excel**:
  - Functions such as `AVERAGE()` and `MEDIAN()` were used for basic summaries. Pivot tables were utilized for grouping and aggregating data.

## Conclusion

- **Stocks** and **Cryptocurrencies** exhibit the highest growth and volatility, making them key market drivers in recent years.
- **Indices** and **Metals** have shown stable price patterns, reflecting their less volatile nature.
- The **trading volumes** were highest for **Indices**, while **Cryptocurrencies** and **Stocks** had high average prices but with more variability in trade volume.

These insights help investors understand the price and volume behavior of different assets, aiding in better portfolio diversification strategies.

## How to Run

1. Install libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

2. Analyze the dataset using Python:
   ```python
   # Import necessary libraries
   import pandas as pd

   # Load dataset
   stock_data = pd.read_csv('path_to_file.csv')

   # Perform basic analysis
   grouped_data = stock_data.groupby('Security (group)').agg(
       avg_price=('Price', 'mean'),
       median_volume=('Vol.', 'median')
   )
   ```

## That's it for my analysis!
I'm always looking to work on projects to further my skills, in the future, I will use better methods, more advanced functions, and some machine learning techniques for better analysis.
