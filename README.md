

This minimalist README.md is strictly based on the actions performed in your Jupyter Notebook and the specific tools you used.

Customer Shopping Behavior Analysis
An end-to-end data pipeline to analyze customer purchasing patterns using Python, PostgreSQL, and Power BI.

🚀 Workflow
1. Data Cleaning & ETL (Python)
Processed raw transaction data using Pandas to ensure consistency and analytical readiness:

Missing Values: Imputed Review Rating using category-specific median values.

Data Standardization: Normalized column headers to snake_case for database compatibility.

Feature Engineering: * Binned age into four segments: Young Adult, Adult, Middle-aged, and Senior.

Mapped qualitative purchase frequencies to numeric day values.

Integration: Automated data export to PostgreSQL using SQLAlchemy.

2. Database Management (PostgreSQL)
Stored cleaned data in a relational database to enable structured querying:

Imported transformed data into a dedicated customer table.

Conducted SQL queries to extract metrics for visualization.

3. Visualization (Power BI)
Connected the PostgreSQL database to Power BI to build an interactive dashboard:

Sales Metrics: Analyzed purchase amounts by category and location.

Customer Profiling: Visualized shopping trends across gender, age groups, and payment methods.

Review Analysis: Tracked product performance based on customer ratings.

🛠️ Tech Stack
Language: Python (Pandas, NumPy)

Database: PostgreSQL

ETL/ORM: SQLAlchemy, Psycopg2

BI Tool: Power BI

Environment: Jupyter Notebook

📂 Project Structure
customer_behaviour.ipynb: Data cleaning and SQL export script.

customer_shopping_behavior.csv: Raw dataset.

customer_behaviour_visuals.pbix: Power BI dashboard file.
