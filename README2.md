
# ABC-XYZ Inventory Classification Analysis

This project presents an analytical approach to inventory management using ABC and XYZ classification techniques. The analysis helps prioritize inventory control strategies by evaluating items based on their consumption value (ABC) and demand variability (XYZ).

---

## 📊 Project Overview

Efficient inventory management is crucial for optimizing stock levels, reducing holding costs, and ensuring availability of materials. This project applies ABC-XYZ classification to a dataset of inventory transactions, enabling data-driven decision-making for supply chain and procurement professionals.

### ABC Classification
- **A Class**: High consumption value, tight control.
- **B Class**: Moderate value, moderate control.
- **C Class**: Low value, minimal control.

### XYZ Classification
- **X Class**: Low demand variability, predictable usage.
- **Y Class**: Moderate variability.
- **Z Class**: High variability, less predictable.

The combined 3x3 ABC-XYZ matrix identifies which items require the most attention in terms of inventory policies (e.g., AX = high priority, CZ = low priority).

---

## 📂 Dataset Description

The dataset consists of historical inventory transaction records with the following fields:

| Column         | Description |
|----------------|-------------|
| `Invoice_No`   | Unique invoice identifier for each transaction. |
| `Item_Code`    | Unique code for each inventory item. |
| `Item_Description` | Text description of the inventory item. |
| `Quantity`     | Number of units sold/ordered in the transaction. |
| `UnitPrice`    | Price per unit of the item. |
| `CustomerID`   | Identifier for the customer placing the order. |
| `Invoice_Date` | Date of the invoice or transaction. |

> The data is aggregated monthly to analyze item consumption trends and compute annual consumption values and demand variability.

---

## 🧪 Methodology

1. **Data Preprocessing**
   - Cleaning missing values and converting date fields.
   - Aggregating item-level monthly consumption.

2. **ABC Classification**
   - Based on total annual consumption value (`Quantity × UnitPrice`).
   - Grouped into A, B, and C based on cumulative percentage.

3. **XYZ Classification**
   - Based on coefficient of variation (CV) of monthly consumption.
   - Items grouped into X, Y, Z based on variability thresholds.

4. **ABC-XYZ Matrix**
   - Merged classification to form 9 item categories (AX, AY, ..., CZ).
   - Visualized using heatmaps and summary tables.

---

## 📌 Key Findings

- 13% of items were classified as **AX** — high value and predictable demand.
- **CZ** items made up 35% — low value and highly unpredictable.
- Targeting AX/AY items for strict control can enhance inventory performance.

---

## 🛠️ Technologies Used

- Python 3.x
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`
- Jupyter Notebook

---

## 📈 Output

- Cleaned and aggregated dataset for analysis.
- Classification plots and heatmaps.
- Final CSV containing ABC, XYZ, and combined classifications.

---

## 🚀 Getting Started

### Prerequisites
Install required Python packages using:

```bash
pip install -r requirements.txt
```

### Run Analysis
Open the Jupyter Notebook and run all cells:
```bash
jupyter notebook abc_xyz_analysis.ipynb
```

---

## 📚 Use Cases

- Inventory prioritization and control
- Demand forecasting
- Stock review policy design
- Procurement planning

---

## 📝 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## 🙌 Acknowledgements

Special thanks to inventory planners and supply chain experts who inspired this project and guided the methodology behind ABC-XYZ classification.