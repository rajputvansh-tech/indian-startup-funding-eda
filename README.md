​🚀 Indian Startup Funding - Exploratory Data Analysis (EDA)

​📌 Project Overview
​This repository contains an Exploratory Data Analysis (EDA) performed on the Indian Startup Funding dataset (startup_funding.csv). 
The goal of this project is to clean, transform, and analyze raw investment records to uncover market trends across startup locations, funding stages, industry sectors, and top investors.

​🛠️ Tech Stack & Libraries
​Language: Python
​Libraries: Pandas, Matplotlib, NumPy
​IDE: Visual Studio Code
​🔑 Key Workflow & Technical Steps
​1. Data Inspection & Health Checks
​Evaluated dataset structure, data types, and total entries using .info() and .describe().
​Assessed missing values across crucial features (AmountInUSD, CityLocation, InvestmentType).

​2. Data Cleaning & Standardization
​Cleaned missing categorical variables and handled NaN values using .fillna().
​Standardized string formatting across city names, investor names, and industry verticals.

​3. Currency & Numerical Conversions
​Handled messy string funding values by removing special characters, commas, and currency symbols ($, \) using regex operations (.replace(..., regex=True)).
​Converted raw funding text into numeric data types (float64) to enable mathematical aggregations.

​4. Advanced Aggregations & Analytics
​Applied .groupby() and .sort_values() to extract key business insights:
​Geographic Distribution: Top startup hubs by total investment.

​Funding Stages: Breakdown of Private Equity, Seed Funding, and Series rounds.
​Sector Analysis: Dominant industry verticals receiving capital.

​Top Startups: Identification of highest funded ventures.

​5. Data Visualization
​Built a grid of side-by-side subplots using plt.subplots() to visualize categorical distributions and funding trends clearly.
​📊 Visual Preview
​Check out the full workflow snapshot:

​📂 Repository Structure

├── data/
│   └── startup_funding.csv        # Raw dataset
├── notebooks/
│   └── startup_funding_eda.py     # Main Python analysis script
├── README.md                      # Project Documentation



🤝 Connect & Feedback
​If you have any feedback, suggestions, or questions regarding this analysis, feel free to reach out or open an issue!


LinkedIn: [https://www.linkedin.com/in/rajputvansh/]

PROJECT LINKS :[https://1drv.ms/u/c/FEEE674F7B0FD6A0/IQBsM8NUCqV0RblaWiyqu0rqAZOEs9buhUzV_SfjhruZIro?e=eg3s3B]


DASHBOARD LINKS:[https://img.sanishtech.com/u/4cfec19730b1506c3cefbec2611367b3.jpg]


