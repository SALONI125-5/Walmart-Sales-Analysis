# Walmart Sales Analysis: End-to-End SQL + Python 

## Project Overview

This project performs an end to end analysis of walmart sales data using python, pandas, MySQL, and SQL. The project covers data cleaning, transformation, EDA, database loading and SQL based business analysis. The obejective is to identify sales trends, customer purchasing patterns, product performance and other business insigths from the dataset.

---

## Project Steps

### 1. Set Up the Environment
   - **Tools Used**: Visual Studio Code (VS Code), Python, SQL (MySQL and PostgreSQL)
   - **Goal**: Create a structured workspace within VS Code and organize project folders for smooth development and data handling.

### 3. Dataset
   - **Data Source**:  Walmart sales dataset from Kaggle.

### 4. Install Required Libraries and Load Data
   - **Libraries**: Install necessary Python libraries using:
     ```bash
     pip install pandas numpy sqlalchemy mysql-connector-python psycopg2
     ```
   - **Loading Data**: Read the data into a Pandas DataFrame for initial analysis and transformations.

### 5. Explore the Data
   - **Goal**: Conduct an initial data exploration to understand data distribution, check column names, types, and identify potential issues.
   - **Analysis**: Use functions like `.info()`, `.describe()`, and `.head()` to get a quick overview of the data structure and statistics.

### 6. Data Cleaning
   - **Remove Duplicates**: Identify and remove duplicate entries to avoid skewed results.
   - **Handle Missing Values**: Drop rows or columns with missing values if they are insignificant; fill values where essential.
   - **Fix Data Types**: Ensure all columns have consistent data types (e.g., dates as `datetime`, prices as `float`).
   - **Currency Formatting**: Use `.replace()` to handle and format currency values for analysis.
   - **Validation**: Check for any remaining inconsistencies and verify the cleaned data.

### 7. Feature Engineering
   - **Create New Columns**: Calculate the `Total Amount` for each transaction by multiplying `unit_price` by `quantity` and adding this as a new column.
   - **Enhance Dataset**: Adding this calculated field will streamline further SQL analysis and aggregation tasks.

### 8. Load Data into MySQL and PostgreSQL
   - **Set Up Connections**: Connect to MySQL and PostgreSQL using `sqlalchemy` and load the cleaned data into each database.
   - **Table Creation**: Set up tables in both MySQL and PostgreSQL using Python SQLAlchemy to automate table creation and data insertion.
   - **Verification**: Run initial SQL queries to confirm that the data has been loaded accurately.

### 9. SQL Analysis: Complex Queries and Business Problem Solving
   - **Business Problem-Solving**: Write and execute complex SQL queries to answer critical business questions, such as:
     - Revenue trends across branches and categories.
     - Identifying best-selling product categories.
     - Sales performance by time, city, and payment method.
     - Analyzing peak sales periods and customer buying patterns.
     - Profit margin analysis by branch and category.
   - **Documentation**: Keep clear notes of each query's objective, approach, and results.

### 10. Project Publishing and Documentation
   - **Documentation**: Maintain well-structured documentation of the entire process in Markdown or a Jupyter Notebook.
   - **Project Publishing**: Publish the completed project on GitHub or any other version control platform, including:
     - The `README.md` file (this document).
     - Jupyter Notebooks (if applicable).
     - SQL query scripts.
     - Data files (if possible) or steps to access them.

---

## Requirements

- **Python 3.8+**
- **SQL Databases**: MySQL, PostgreSQL
- **Python Libraries**:
  - `pandas`, `numpy`, `sqlalchemy`, `mysql-connector-python`, `psycopg2`

## Getting Started

1. Clone the repository:
   ```bash
   git clone <repo-url>
   ```
2. Install Python libraries:
   ```bash
   pip install -r requirements.txt
3  Open project.ipynb and run the notebook for data cleaning and transformation.
4  Run the python notebook for data cleaning and analysis.
5  Load the cleaned data into MySQL.
6  Execute the SQL queries in mysql_queries.sql.   ```

---
## Project Structure

```plaintext
Walmart Sales Analysis/
│
├── MySQL Queries.sql              # SQL queries for business analysis using MySQL
├── project.ipynb                  # Jupyter notebook for data cleaning, analysis
├── PSQL Queries.sql               # SQL queries for business analysis using PostgreSQL
├── README.md                      # Project documentation and analysis results
├── requirements.txt               # List of required Python libraries
├── Walmart.csv                    # Original Walmart sales dataset
├── walmart_clean_data.csv         # Cleaned and transformed Walmart sales dataset
├── Walmart Project.png            # Project overview and workflow diagram
└── Walmart Project-pipelines.png  # Data processing and project pipeline diagram
---

## Results and Insights

The analysis of Walmart sales data produced the following key findings:

### Key Results

- *Payment Methods:* Three payment methods were identified: Credit Card, Ewallet, and Cash. Credit Card recorded the highest quantity of items sold with *9,567 items, followed by Ewallet (8,932) and Cash (4,984*).

- *Highest-Rated Category by Branch:* The analysis identified the highest-rated product category for each Walmart branch based on average customer ratings. This helped identify branch-level differences in customer preferences and satisfaction.

- *Busiest Day by Branch:* The busiest day of the week was determined for each branch based on transaction volume. The results showed that peak days vary across branches, providing useful information for staffing and inventory planning.

- *Quantity Sold by Payment Method:* A total of *23,483 items* were sold across the three payment methods. Credit Card accounted for the largest quantity (*9,567), followed by Ewallet (8,932) and Cash (4,984*).

- *Category Ratings by City:* The analysis calculated the minimum, maximum, and average rating for each product category across cities, resulting in *513 city-category combinations*. The results showed variations in customer ratings across different locations and product categories.

- *Profit by Category:* Fashion accessories generated the highest profit of approximately *192,314.89, closely followed by Home and lifestyle at **192,213.64. Electronic accessories generated approximately **30,772.49, while Health and beauty generated the lowest profit among the categories at approximately **18,671.73*.

- *Most Common Payment Method by Branch:* The most frequently used payment method was identified for each branch. Ewallet and Credit Card appeared as the most common payment methods across the displayed branch results, indicating differences in payment preferences between branches.

- *Sales by Time of Day:* Transactions were categorized into Morning, Afternoon, and Evening. The displayed results generally showed higher transaction activity during the *Afternoon*, while Morning had comparatively lower activity across several branches.

- *Year-over-Year Revenue Decline:* The analysis compared branch-level revenue between 2022 and 2023. *WALM045* experienced the highest revenue decline at *62.62%, followed by **WALM047 (58.58%), **WALM098 (57.89%), **WALM033 (55.65%), and **WALM081 (50.67%)*.

### Business Insights

- Customer payment preferences vary across Walmart branches.
- Afternoon appears to be an important period for transaction activity, which can support staffing and inventory planning.
- Customer ratings differ across cities and product categories, indicating regional differences in customer preferences.
- Fashion accessories and Home and lifestyle were the strongest categories in terms of calculated profit.
- Several branches experienced substantial year-over-year revenue declines, highlighting areas that may require further investigation.
- Branch-level analysis can help Walmart make more targeted decisions regarding inventory, staffing, promotions, payment options, and sales strategies.

## Acknowledgments

- **Data Source**: Kaggle’s Walmart Sales Dataset
- **Inspiration**: Walmart’s business case studies on sales and supply chain optimization.

---
