

Customer Shopping Behavior: End-to-End Data Analysis Project
📌 Project Overview
This project focuses on analyzing customer shopping patterns to derive actionable insights for retail businesses. The workflow covers the entire data lifecycle: from raw data cleaning and transformation in Python, storage and querying in PostgreSQL, to interactive data visualization in Power BI.
🛠️ Tech Stack
•	Language: Python 3.x
•	Libraries: Pandas, NumPy, SQLAlchemy, Psycopg2
•	Database: PostgreSQL
•	Visualization: Power BI
•	Environment: Jupyter Notebook
📂 Dataset Description
The dataset contains 3,900 records of customer transactions, including:
•	Demographics: Age, Gender, Location.
•	Transaction Details: Item Purchased, Category, Purchase Amount (USD), Season.
•	Customer Loyalty: Subscription Status, Previous Purchases, Frequency of Purchases.
•	Feedback: Review Ratings.
________________________________________
⚙️ Data Pipeline
1. Data Cleaning & Transformation (Python)
Using Pandas in a Jupyter Notebook, I performed the following steps to ensure data quality and readiness for SQL:
•	Missing Value Treatment: Identified null values in Review Rating and imputed them using the median rating of their respective product categories.
•	Standardization: Converted column names to lowercase and replaced spaces with underscores (e.g., Purchase Amount (USD) → purchase_amount) for seamless SQL integration.
•	Feature Engineering:
o	Age Grouping: Categorized customers into Young Adult, Adult, Middle-aged, and Senior using quantile-based binning (pd.qcut).
o	Frequency Mapping: Converted categorical frequency (e.g., "Weekly", "Fortnightly") into numeric purchase_frequency_days for quantitative analysis.
•	Redundancy Removal: Dropped columns like promo_code_used that didn't add unique value to the analysis.

2. Database Management (PostgreSQL)
After cleaning, the data was exported to a PostgreSQL database using the SQLAlchemy engine.
•	Workflow: Automated the table creation and data insertion process from Python.
•	SQL Analysis: Executed queries to identify high-value customers, regional sales trends, and seasonal performance.
•	Sample Query: ```sql SELECT category, SUM(purchase_amount) as total_sales FROM customer GROUP BY category ORDER BY total_sales DESC;
•	
3. Data Visualization (Power BI)
The PostgreSQL database was connected to Power BI to create a dynamic dashboard. Key visuals include:
•	Sales Overview: Total Revenue ($233k) and Total Purchases.
•	Category Performance: Analysis showing Clothing as the lead revenue generator ($104k+).
•	Customer Segmentation: Breakdown of spending by Gender and Age Group.
•	Regional Insights: A map visualization showing top-performing states.
________________________________________
📈 Key Insights
•	Top Category: Clothing is the most popular and profitable category, followed by Accessories.
•	Customer Demographics: Spending is remarkably balanced between Male and Female customers, suggesting a broad market appeal.
•	Age Trends: The "Young Adult" segment represents a significant portion of the customer base, followed closely by "Middle-aged" shoppers.
•	Revenue: The total generated revenue from the analyzed period stands at $233,081.
🚀 How to Run
1.	Python: Run the customer_behaviour.ipynb to clean the data and push it to your local PostgreSQL instance.
2.	SQL: Use the customer table in PostgreSQL to run analytical queries.
3.	Power BI: Open customer_behaviour_visuals.pbix and refresh the data source to see the updated visuals (ensure your PostgreSQL service is running).





________________________________________
📝 Final Thoughts
This project demonstrates a robust understanding of the data engineering and analysis process. By moving data from a flat file (CSV) to a relational database (SQL) and finally to a BI tool, I've created a scalable solution for business intelligence.
________________________________________


 

	


