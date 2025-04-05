# ABC XYZ Inventory Classification Analysis

This repository contains a data analytics project on inventory classification using the **ABC** and **XYZ** techniques. The goal of the analysis is to help organizations optimize inventory management by categorizing items based on their consumption value and demand variability.

## 📊 Project Overview

Inventory classification is crucial for efficient stock control and inventory optimization. This project uses real-world inventory data and applies:

- **ABC Analysis** (based on Pareto Principle – 80/20 rule)
- **XYZ Analysis** (based on demand variability measured by Coefficient of Variation)

Combining both methods (ABC-XYZ matrix) helps prioritize items for planning, control, and purchasing decisions.

## ✅ Key Objectives

- Improve inventory management practices.
- Minimize stock-outs and reduce holding costs.
- Provide insights for better decision-making in procurement and storage.

## 🛠️ Methodology

1. **Data Preprocessing**:
   - Cleaned inventory transaction data.
   - Calculated yearly consumption value per item.
   - Computed mean and standard deviation of demand.

2. **ABC Classification**:
   - Categorized items into:
     - A (high value)
     - B (moderate value)
     - C (low value)

3. **XYZ Classification**:
   - Based on Coefficient of Variation (CV = σ / μ):
     - X (low variability)
     - Y (moderate variability)
     - Z (high variability)

4. **ABC-XYZ Matrix**:
   - Combined categories (e.g., AX, BY, CZ) to create a 3x3 matrix for comprehensive inventory insights.

## 📈 Tools & Technologies

- Python (NumPy, Pandas, Matplotlib, Seaborn)
- Jupyter Notebook
- Excel (for initial data visualization and sorting)

## 📂 Files in this Repository

- `abc_xyz_analysis.ipynb`: Jupyter Notebook containing all code and visualizations.
- `inventory_data.csv`: Cleaned inventory data used for analysis.
- `ABC XYZ Inventory Classification Analysis.pdf`: Project report detailing objectives, process, findings, and conclusions.
- `README.md`: Project overview and setup instructions.

## 📊 Key Findings

- Identified critical items (AX category) that need close monitoring.
- Segmented less critical items (CZ) to apply minimal control.
- Demonstrated how the combined classification helps in prioritizing inventory control efforts.

## 📚 Use Case

This project is ideal for:
- Supply chain analysts
- Inventory planners
- Procurement and operations teams
- Educational purposes in operations management

## 🤝 Contributions

Feel free to fork this repository, raise issues, or submit pull requests if you'd like to contribute or improve upon the analysis.

## 📃 License

This project is licensed under the MIT License.

---

**Author**: [Your Name]  
**Date**: April 2025
