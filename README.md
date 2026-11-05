# Diwali Sales Data Analysis

[![Python](https://img.shields.io/badge/Python-3.14+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Data_Visualization-4C72B0?style=for-the-badge)](https://seaborn.pydata.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

An end-to-end Exploratory Data Analysis (EDA) project on customer purchases during the festive season of Diwali. This analysis uncovers retail patterns, customer demographics, geographical spending distribution, and high-revenue product categories to assist businesses in optimizing sales strategies and inventory planning.

---

## Table of Contents
- [Executive Summary](#executive-summary)
- [Key Insights and Findings](#key-insights-and-findings)
- [Dataset Overview](#dataset-overview)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
  - [1. Gender Analysis](#1-gender-analysis)
  - [2. Age Demographics](#2-age-demographics)
  - [3. Geographic and State-wise Spending](#3-geographic-and-state-wise-spending)
  - [4. Regional Zone Breakdown](#4-regional-zone-breakdown)
  - [5. Product Categories across States](#5-product-categories-across-states)
- [Business Recommendations](#business-recommendations)
- [Project Structure](#project-structure)
- [Installation and Setup](#installation-and-setup)
- [Technologies Used](#technologies-used)
- [Author](#author)

---

## Executive Summary

The objective of this project is to analyze transaction data from the Diwali sales festival to identify target customer profiles and high-performing regions and sectors.

> **Key Takeaway:**  
> The core customer segment driving festive sales comprises **married women aged 26-35 years** residing in **Western and Central states (primarily Uttar Pradesh, Maharashtra, and Karnataka)** working in corporate and government sectors, with major spending concentrated in **Food, Clothing and Apparel, and Electronics**.

---

## Key Insights and Findings

| Category | Key Finding |
| :--- | :--- |
| **Gender** | **Females represent the primary purchasing force**, accounting for over **70% of total revenue** (~INR 74.3M vs INR 31.9M by males) and significantly higher order counts. |
| **Age Group** | The **26-35 age group** dominates across both genders, generating the highest total sales and number of orders. |
| **Top States** | **Uttar Pradesh**, **Maharashtra**, and **Karnataka** generate the highest order volume and aggregate spend. |
| **Zone Distribution** | The **Western zone** holds the largest share of orders, followed by Central and Southern regions. |
| **Categories** | **Food**, **Clothing and Apparel**, and **Electronics** are the top three revenue-generating categories. |

---

## Dataset Overview

The dataset (`Diwali Sales Data.csv`) contains **11,251 customer transactions** with 15 attributes:

| Column Name | Description | Data Type |
| :--- | :--- | :--- |
| `User_ID` | Unique identifier for each customer | Integer |
| `Cust_name` | Name of the customer | String |
| `Product_ID` | Unique identifier for each product | String |
| `Gender` | Gender of the customer (`M` / `F`) | String |
| `Age Group` | Categorized age ranges (`0-17`, `18-25`, `26-35`, etc.) | Categorical |
| `Age` | Exact age of the customer | Integer |
| `Marital_Status` | Marital status indicator (`0` = Unmarried, `1` = Married) | Integer |
| `State` | State of residence | String |
| `Zone` | Geographic zone (`Central`, `Southern`, `Western`, `Northern`, `Eastern`) | String |
| `Occupation` | Customer occupation sector | String |
| `Product_Category` | Category of the purchased item | String |
| `Orders` | Quantity of items ordered | Integer |
| `Amount` | Total order amount in INR | Float / Integer |
| `Status` / `unnamed1` | Unused / empty columns | Dropped |

---

## Data Cleaning and Preparation

1. **Encoding Handling:** Loaded using `encoding='unicode_escape'` to correctly read special non-UTF8 characters.
2. **Dropping Redundant Columns:** Removed blank columns `Status` and `unnamed1`.
3. **Handling Missing Values:** Detected and dropped 12 records where `Amount` was null.
4. **Data Type Conversion:** Cast `Amount` from `float64` to `int64` for cleaner metrics and visual presentation.
5. **Formatted Visualizations:** Eliminated scientific notation (`1e7`) across all charts and implemented standard comma-separated numeric labels (`{:,.0f}`).

---

## Exploratory Data Analysis

### 1. Gender Analysis
- **Order Count:** Female shoppers placed significantly more orders than male shoppers.
- **Revenue Generated:** Total female spend exceeds **INR 74.33M**, compared to **INR 31.91M** for males.

### 2. Age Demographics
- Analysis across age bins (`0-17`, `18-25`, `26-35`, `36-45`, `46-50`, `51-55`, `55+`) confirms that **26-35 year-old females** constitute the single largest consumer segment.

### 3. Geographic and State-wise Spending
- **Order Density:** Uttar Pradesh leads in overall transaction count.
- **Top 10 States by Expenditure:**
  1. Uttar Pradesh
  2. Maharashtra
  3. Karnataka
  4. Delhi
  5. Madhya Pradesh
  6. Andhra Pradesh
  7. Himachal Pradesh
  8. Haryana
  9. Bihar
  10. Gujarat

### 4. Regional Zone Breakdown
- **West Zone** commands the largest order share (~28%), closely followed by **Central** and **Southern** zones.

### 5. Product Categories across States
- Pivot tables and heatmaps reveal high expenditure concentration in **Food** and **Clothing and Apparel**, with sustained demand for **Electronics** in high-tier urban states.

---

## Business Recommendations

1. **Targeted Marketing Campaigns:** Allocate higher ad budgets towards female demographics aged 25-35 on digital channels.
2. **Inventory Optimization:** Stock up on Food, Clothing, and Electronics in fulfillment centers serving Uttar Pradesh, Maharashtra, and Karnataka prior to festival peaks.
3. **Festive Bundling:** Introduce combo discounts pairing top-selling food items with festive apparel to increase the average order value (AOV).
4. **Regional Expansion:** Develop localized promotional strategies to tap into underperforming areas such as the Eastern zone.

---

## Project Structure

```text
Diwali-analysis/
|-- Diwali Sales Data.csv        # Dataset containing customer transaction records
|-- Diwali_Sales_Analysis.ipynb  # Jupyter Notebook containing full EDA and visualizations
|-- .gitignore                   # Excludes virtual environments, caches, and system files
`-- README.md                    # Comprehensive project documentation
```

---

## Installation and Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/mohamedmohabcv111-oss/Diwali_Analysis.git
   cd Diwali_Analysis
   ```

2. **Create and activate a virtual environment:**
   ```bash
   # Windows (PowerShell)
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1

   # macOS / Linux
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install required packages:**
   ```bash
   pip install numpy pandas matplotlib seaborn ipykernel
   ```

4. **Launch the Jupyter Notebook:**
   ```bash
   jupyter notebook Diwali_Sales_Analysis.ipynb
   ```

---

## Technologies Used

- **Language:** Python
- **Environment:** Jupyter Notebook / Visual Studio Code
- **Data Manipulation:** [Pandas](https://pandas.pydata.org/), [NumPy](https://numpy.org/)
- **Data Visualization:** [Matplotlib](https://matplotlib.org/), [Seaborn](https://seaborn.pydata.org/)
- **Version Control:** Git and GitHub

---

## Author

**Mohamed Mohab**  
- GitHub: [@mohamedmohabcv111-oss](https://github.com/mohamedmohabcv111-oss)  
- Email: [mohamedmohabcv111@gmail.com](mailto:mohamedmohabcv111@gmail.com)
