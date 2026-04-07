# World-Data-Exploratory---Python---Panda
Cleaning and optimizing global development indicators for statistical correlation.

Project Overview
-----------------
This project involves a deep-dive exploratory analysis of a global development dataset. The primary objective was to practice Data Profiling, Cleaning, and Statistical Correlation using Python. By analyzing various global indicators, I identified trends and relationships between socio-economic factors across different regions.

Key Objectives
---------------
Data Cleaning: Handle missing values, incorrect data types, and duplicate records.
Type Optimization: Convert "object" types to "float" or "category" to reduce memory usage and enable mathematical operations.
Aggregation: Use groupby and pivot logic to summarize data by continent and year.
Visual Exploration: Create a correlation heatmap to identify which global factors (e.g., GDP vs. Life Expectancy) move together.

Technical Stack
----------------
Language: Python
Libraries: * Pandas: For data manipulation and "Group By" operations.
Seaborn & Matplotlib: For statistical data visualization.

Project Workflow
-----------------
1. Initial Data Profiling
The raw dataset contained over 200 rows and 12+ columns with inconsistent formatting. I began by using df.info() and df.describe() to identify:
. Columns with high percentages of null values.
. Numeric data mistakenly stored as strings (Objects).

3. Data Cleaning & Optimization
Handling Nulls: Applied conditional filling for missing values based on regional averages.
Memory Management: Utilized .select_dtypes(include="float") to isolate and verify technical metrics.
Standardization: Cleaned country names and region headers for consistent grouping.

4. Statistical Analysis
I performed a Correlation Analysis to see how strongly different indicators were linked.Key Finding: There was a strong positive correlation ($r > 0.7$) between specific economic indicators and healthcare outcomes.Aggregation: Analyzed the "Top 10" and "Bottom 10" countries in various categories using sort_values and head().

Key Insights
-------------
Data Skewness: Significant outliers were found in GDP data, requiring logarithmic scaling for better visualization.
Regional Trends: Grouping the data revealed that certain geographic regions showed 2x more volatility in growth metrics compared to others.
Optimization: By converting data types correctly, I reduced the processing memory footprint by nearly 30%.

How to Run
-----------
. Clone this repository.
. Ensure you have the dataset file (CSV/Excel) in the same directory.
. Install dependencies: pip install pandas seaborn matplotlib
. Open Exploratory_Pandas.ipynb in Jupyter Notebook or VS Code.
