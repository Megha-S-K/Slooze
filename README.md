# 📦 Slooze — Inventory Optimization & Demand Forecasting

> End-to-end data science analysis for a retail wine & spirits company — turning raw transactional data into actionable inventory intelligence.

---

## 🧠 What This Project Does

This project analyzes over **1 million+ sales and procurement records** to help a retail business answer three critical questions:

- **When** should we reorder stock — and how much?
- **Which** products deserve priority inventory investment?
- **Why** is capital getting locked in unsold inventory?

Built as a take-home data science challenge for **Slooze**, this analysis covers the full pipeline — from raw CSV ingestion to business recommendations.

---

## 📊 Key Results

| Analysis | Result | Business Impact |
|---|---|---|
| Demand Forecasting (7-day MA) | Feb demand dropped after Jan peak | Avoid over-ordering in low seasons |
| ABC Classification | 36K high-value "A" products identified | Focus stock investment on what sells |
| Avg Supplier Lead Time | **7.6 days** | Plan orders at least 8 days in advance |
| Reorder Point | **~311,328 units** | Trigger restocking before stockouts hit |
| Inventory Turnover Ratio | **0.53** (slow movement) | Reduce C-category overstock, free up capital |

---

## 🔍 Analysis Breakdown

### 1. Demand Forecasting
Aggregated daily sales and applied a **7-day moving average** to smooth noise and identify trends. Found a clear seasonal dip in February — useful for purchase planning.

### 2. ABC Inventory Classification
Classified ~170K products by revenue contribution:
- **A (36,801 products)** → High value, priority stocking
- **B (48,205 products)** → Medium importance
- **C (85,125 products)** → Low value, reduce excess stock

### 3. Lead Time Analysis
Calculated `Lead Time = Receiving Date − Purchase Order Date` across all suppliers.
Average: **7.6 days** — giving procurement teams a concrete planning window.

### 4. Reorder Point Calculation
```
Reorder Point = Avg Daily Demand × Avg Lead Time
             = 40,852 units/day × 7.6 days
             ≈ 311,328 units
```
When inventory hits this threshold, a new order must be placed to prevent stockouts.

### 5. Inventory Turnover
```
Turnover Ratio = Total Sales Qty / Avg Inventory = 0.53
```
A ratio below 1 indicates overstocking — capital tied up in products that aren't moving fast enough.

---

## 🗂 Datasets Used

| File | Description |
|---|---|
| `SalesFINAL12312016.csv` | Customer sales transactions & revenue |
| `PurchasesFINAL12312016.csv` | Procurement & supplier delivery data |
| `BegInvFINAL12312016.csv` | Inventory levels at period start |
| `EndInvFINAL12312016.csv` | Inventory levels at period end |

> Datasets are not included in this repo. Place CSV files in the root directory before running.

---

## 🛠 Tech Stack

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Jupyter Notebook`

---

## 🚀 Run Locally

```bash
# 1. Clone the repo
git clone https://github.com/Megha-S-K/Slooze.git
cd Slooze

# 2. Install dependencies
pip install pandas numpy matplotlib jupyter

# 3. Add dataset CSVs to the root folder

# 4. Launch notebook
jupyter notebook inventory_analysis.ipynb
```

Run all cells top to bottom to reproduce the full analysis.

---

## 💡 Key Takeaways

- Demand is **seasonal** — procurement must adapt, not follow fixed schedules
- A small fraction of products drives most revenue — **prioritize them**
- Low inventory turnover = **capital locked in dead stock** — needs active management
- A data-driven reorder point prevents both **stockouts and overstocking**
