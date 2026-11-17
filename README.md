​# 🚀 Indian Startup Funding — Exploratory Data Analysis (EDA)

An end-to-end Exploratory Data Analysis (EDA) project analyzing the **Indian Startup Funding ecosystem** (`startup_funding.csv`). Built using **Python (Pandas, NumPy, Matplotlib)**, this project cleans raw financial records, resolves missing values and city naming inconsistencies, and visualizes top-performing cities, investment types, yearly trends, industry verticals, and funded startups.

---

## 📊 Executive Summary & Dashboard

![Indian Startup Funding Dashboard](YOUR_PERMANENT_GITHUB_IMAGE_LINK_HERE)

---

## 📁 Dataset Overview (`startup_funding.csv`)

- **Total Records:** 3,044 rows  
- **Original Columns (10):** `Sr No`, `Date dd/mm/yyyy`, `Startup Name`, `Industry Vertical`, `SubVertical`, `City Location`, `Investors Name`, `InvestmentnType`, `Amount in USD`, `Remarks`
- **Data Cleaning Highlights:**
  - Dropped the sparse `Remarks` column (only 419 non-null entries out of 3,044).
  - Standardized column names (`Amount`, `name`, `industry vertical`, `type`, `city`, `date`).
  - Handled missing values across categorical columns (`industry vertical`: 171 nulls, `SubVertical`: 936 nulls, `city`: 180 nulls, `type`: 4 nulls, `Investors Name`: 24 nulls) by imputing `'unknown'`.
  - Cleaned the `Amount` column (`960` missing entries) by stripping commas (`,`), converting string figures to numeric (`float64`), and replacing non-numeric/missing entries with `0`.
  - Standardized city names by replacing `'Bengaluru'` with `'Bangalore'` to consolidate funding metrics accurately.

---

## 🔍 Detailed Analytical Insights (From Code & Dashboard)

### 1. 🏙️ Top 5 Cities by Total Funding & Deal Volume
Bangalore dominates the Indian startup ecosystem both in capital raised and total deal frequency, holding a massive lead over Mumbai and the NCR region.

| Rank | City | Total Funding (USD) | Approx. Value | Deal Count |
| :--- | :--- | :---: | :---: | :---: |
| **1** | **Bangalore** | `$18,469,868,863` | **~$18.47 Billion** | 842 deals |
| **2** | **Mumbai** | `$4,921,185,015` | **~$4.92 Billion** | 568 deals |
| **3** | **New Delhi** | `$3,017,816,875` | **~$3.02 Billion** | 424 deals |
| **4** | **Gurgaon** | `$3,006,496,134.5` | **~$3.01 Billion** | 341 deals |
| **5** | **Unknown** | `$1,271,813,868` | **~$1.27 Billion** | 180 deals |

- **Key Takeaway:** Bangalore alone accounts for **over 3.7x** the funding of runner-up Mumbai. Combined, Delhi NCR (New Delhi + Gurgaon) attracts ~$6.02B, making it the second-largest regional hub after Bangalore.

---

### 2. 💰 Top 5 Investment Types by Capital Volume
Late-stage institutional capital drives the vast majority of funding volume compared to early-stage rounds.

| Rank | Investment Type | Total Funding (USD) | Approx. Value |
| :--- | :--- | :---: | :---: |
| **1** | **Private Equity** | `$26,642,318,185` | **~$26.64 Billion** |
| **2** | **Series B** | `$4,799,095,735` | **~$4.80 Billion** |
| **3** | **Series D** | `$1,481,799,000` | **~$1.48 Billion** |
| **4** | **Series C** | `$1,044,718,394` | **~$1.04 Billion** |
| **5** | **Funding Round** | `$1,000,000,000` | **~$1.00 Billion** |

- **Key Takeaway:** **Private Equity** accounts for the lion's share of total capital deployed (**~$26.64B**), outpacing Series B, C, and D combined. This indicates heavy capital concentration in mature, scaling unicorns.

---

### 3. 📅 Top 5 Years by Funding Volume
Funding peaked in **2017**, followed closely by **2019** and **2015**, showing cyclical surges driven by mega-rounds in e-commerce and fintech.

| Rank | Year | Total Funding (USD) | Approx. Value |
| :--- | :--- | :---: | :---: |
| **1** | **2017** | `$10,429,309,730` | **~$10.43 Billion** |
| **2** | **2019** | `$9,686,577,415` | **~$9.69 Billion** |
| **3** | **2015** | `$8,597,202,368` | **~$8.60 Billion** |
| **4** | **2018** | `$5,122,368,369` | **~$5.12 Billion** |
| **5** | **2016** | `$3,828,088,608` | **~$3.83 Billion** |

- **Key Takeaway:** After a dip in 2016 (~$3.83B), investments rebounded sharply by **172% in 2017 (~$10.43B)**—the highest single-year inflow in the dataset.

---

### 4. 🏭 Top 5 Industry Verticals
Consumer-facing digital platforms and mobility services captured the highest investor interest.

| Rank | Industry Vertical | Total Funding (USD) | Approx. Value |
| :--- | :--- | :---: | :---: |
| **1** | **Consumer Internet** | `$6,253,084,245` | **~$6.25 Billion** |
| **2** | **eCommerce** | `$5,002,533,000` | **~$5.00 Billion** |
| **3** | **Transportation** | `$3,916,632,394` | **~$3.92 Billion** |
| **4** | **Technology** | `$2,229,707,930` | **~$2.23 Billion** |
| **5** | **Finance** | `$1,971,438,000` | **~$1.97 Billion** |

- **Key Takeaway:** **Consumer Internet (~$6.25B)** and **eCommerce (~$5.00B)** together attracted over **$11.25 Billion**, reflecting rapid smartphone and internet adoption across India.

---

### 5. Unicorn Leaders: Top 5 Funded Startups
A handful of market-leading startups absorbed multi-billion-dollar investments, skewing the overall funding distribution.

| Rank | Startup Name | Total Funding (USD) | Approx. Value |
| :--- | :--- | :---: | :---: |
| **1** | **Flipkart** | `$4,059,700,000` | **~$4.06 Billion** |
| **2** | **Rapido Bike Taxi** | `$3,900,000,000` | **~$3.90 Billion** |
| **3** | **Paytm** | `$3,148,950,000` | **~$3.15 Billion** |
| **4** | **Ola** | `$984,500,000` | **~$984.50 Million** |
| **5** | **Udaan** | `$870,000,000` | **~$870.00 Million** |

- **Key Takeaway:** **Flipkart (~$4.06B)**, **Rapido Bike Taxi (~$3.90B)**, and **Paytm (~$3.15B)** each crossed the $3B mark, leading the e-commerce, mobility, and digital payments revolutions respectively.

---

## 🛠️ Tech Stack & Libraries Used

- **Language:** Python 3.14
- **Data Manipulation & Cleaning:** `Pandas`, `NumPy`
- **Data Visualization:** `Matplotlib` (`1x5` subplot grid comparing top 5 metrics)
- **Environment:** Visual Studio Code

---

DASHBOARD:[https://imglink.cc/cdn/STAg8t-Hwr.jpg]
