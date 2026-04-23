![Teleco Churn Dashboard](dashboard_overview.png)
Telco Customer Churn Analysis
Project Overview
This project focuses on identifying patterns in customer attrition (churn) within the telecommunications sector. The primary goal was to take a raw, inconsistent dataset and transform it into a structured analytical model to visualize churn drivers and revenue impact through an interactive Power BI dashboard.

Key Technical Features
End-to-End Data Transformation: Cleaned and normalized "unclean" source data using Power Query.

Advanced DAX Modeling: Developed custom measures to track business KPIs like Churn Rate and Revenue at Risk.

Predictive Insights: Segmented customers by tenure and service usage to identify high-risk profiles.

Data Transformation (Power Query)
The raw dataset (telco_churn_unclean.csv) required significant refinement before it could be used for analysis. The following steps were implemented in the Power Query editor:

Numerical Standardization:

Cleaned MonthlyCharges and TotalCharges by removing currency symbols (e.g., $) and non-numeric characters.

Changed data types to Decimal Number to allow for mathematical calculations.

Handled null values and empty strings in revenue columns to ensure model accuracy.

Categorical Normalization:

Standardized inconsistent text entries in the Contract column (e.g., merging "month to month" with "Month-to-month").

Trimmed whitespace and corrected naming conventions in PaymentMethod.

Feature Engineering:

Created Tenure Buckets (e.g., 0-12 Months, 1-2 Years) to analyze how customer loyalty changes over time.

Added conditional columns to simplify service offerings into "Yes/No" categories for better filtering.

Analytical Measures (DAX)
To drive the dashboard's intelligence, I developed several key measures:

Churn Rate %: DIVIDE(CALCULATE(COUNT(Churn), Churn="Yes"), COUNT(Churn))

Revenue at Risk: Quantifies the total TotalCharges associated with customers who have already churned.

Average Monthly Revenue: Provides insights into the value of different customer segments.

Dashboard Insights
Contract Influence: Month-to-month subscribers represent the highest churn risk, suggesting a need for long-term incentive programs.

Service Quality: Customers using Fiber Optic services show higher churn rates compared to DSL, indicating potential issues with pricing or service stability in that segment.

Retention Drivers: Customers with "Tech Support" and "Online Security" add-ons have significantly higher retention rates.

How to Explore
Raw Data: View the initial state in telco_churn_unclean.csv.

Power BI Report: Open Telco_Churn.pbix in Power BI Desktop to interact with the visuals and review the DAX measures.

Tools Used
Power BI Desktop: Reporting and Visualization.

Power Query: ETL (Extract, Transform, Load) processes.

DAX: Advanced analytical calculations.
