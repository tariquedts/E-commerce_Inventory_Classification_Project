# Inventory Classification Using ABC-XYZ Analysis

### Overview
This project applies data science to inventory management, helping businesses optimize stock levels and improve profitability.
This project implements a data-driven inventory classification system using the ABC-XYZ analysis method. ABC categorizes stock based on revenue contribution, while XYZ classifies items by demand predictability. By combining these methods, businesses can make informed inventory management decisions to optimize stock levels, reduce holding costs, and improve profitability.

### Table of Contents
- [Introduction](#introduction)
- [How ABC-XYZ Inventory Classification Works](#how-abc-xyz-inventory-classification-works)
- [Project Workflow](#project-workflow)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Results and Insights](#results-and-insights)
- [Future Improvements](#future-improvements)
- [How to Use the Code](#how-to-use-the-code)

### Introduction
Inventory classification is essential for effective supply chain management. This project demonstrates how ABC and XYZ analysis can be combined to classify inventory items based on revenue and demand consistency.

### How ABC-XYZ Inventory Classification Works
#### **ABC Classification (Revenue-Based Segmentation)**
- **A Items:** High-value, low-quantity items contributing most to revenue.
- **B Items:** Moderate-value items with a balanced revenue contribution.
- **C Items:** Low-value, high-quantity items contributing the least to revenue.

#### **XYZ Classification (Demand-Based Segmentation)**
- **X Items:** Consistently demanded products with predictable sales patterns.
- **Y Items:** Moderately fluctuating demand, often seasonal.
- **Z Items:** Highly unpredictable demand, requiring strategic stocking decisions.

#### **Combining ABC and XYZ**
By combining ABC and XYZ analysis, inventory items are categorized into nine classes (AX, AY, AZ, BX, BY, BZ, CX, CY, CZ), helping businesses optimize their stock management strategies.

### Project Workflow
#### **1. Data Collection**
- Gather historical sales data from an e-commerce or retail store.
- Key columns: Product ID, Sales Volume, Revenue, Demand Consistency.

#### **2. Data Preprocessing**
- Handle missing values and outliers.
- Convert timestamps to relevant time intervals (e.g., daily, weekly sales).
- Aggregate sales and revenue data.

#### **3. ABC Classification**
- Calculate cumulative revenue percentage.
- Define thresholds for A (top 70%), B (next 20%), and C (bottom 10%) items.

#### **4. XYZ Classification**
- Compute demand variability (Coefficient of Variation: CV = StdDev/Mean).
- Define thresholds:
  - X: CV < 0.5 (Stable demand)
  - Y: 0.5 <= CV < 1 (Moderate fluctuations)
  - Z: CV >= 1 (Unpredictable demand)

#### **5. ABC-XYZ Matrix Formation**
- Combine the ABC and XYZ classifications.
- Generate insights for inventory strategy:
  - **AX Items:** High revenue, stable demand (Ensure availability, minimal stock-outs)
  - **CZ Items:** Low revenue, unpredictable demand (Avoid overstocking)

#### **6. Visualization & Insights**
- Generate bar charts, heatmaps, and scatter plots to visualize classifications.
- Identify inventory optimization opportunities.

#### **7. Implementation & Reporting**
- Export classification results to a structured CSV file.
- Generate recommendations for inventory management based on findings.

### Dataset
The dataset contains:
- `Product_ID`: Unique identifier for each product.
- `Sales_Volume`: Total units sold.
- `Revenue`: Total earnings from the product.
- `Demand_Variability`: Standard deviation of sales over time.
- `Category`: Pre-assigned product category.

### Technologies Used
- **Python (Pandas, NumPy, Matplotlib, Seaborn, Scipy)** – Data processing & visualization.
- **SQL** – Querying and filtering sales data.
- **Excel/Google Sheets** – Exploratory analysis.
- **Jupyter Notebook** – Interactive development.

### Results and Insights
- The **AX category** (high revenue, stable demand) is critical for business profitability and should always be in stock.
- **BZ & CZ categories** (low revenue, fluctuating demand) require careful monitoring to avoid overstocking.
- Seasonal products in **Y categories** need stocking adjustments before peak periods.

### Future Improvements
- Automate real-time ABC-XYZ classification using cloud-based dashboards.
- Integrate with inventory management software.
- Use machine learning for dynamic demand forecasting.

### How to Use the Code
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/inventory-classification.git
   ```
2. Install dependencies:
   ```sh
   pip install pandas numpy matplotlib seaborn
   ```
3. Run the Jupyter Notebook or script:
   ```sh
   python abc_xyz_classification.py
   ```
4. Analyze the output CSV file for classification results.

---

This project applies data science to inventory management, helping businesses optimize stock levels and improve profitability.

