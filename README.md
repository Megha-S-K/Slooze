# Slooze Data Science Take Home Challenge
## Data Science Take-Home Challenge — Inventory Optimization & Demand Forecasting

## 📌 Project Overview

This project performs end-to-end data analysis for a retail wine & spirits company to optimize inventory management, analyze sales and procurement performance, and reduce operational inefficiencies. Using real business datasets, the project applies time-series forecasting, inventory classification, supply chain analysis, and stock optimization techniques to generate actionable business insights.

The goal is to simulate real-world decision making at Slooze by transforming raw transactional data into meaningful operational intelligence.

## 🎯 Business Objectives Addressed

* Inventory Optimization — Determine ideal inventory levels and reorder strategy
* Sales & Purchase Insights — Identify demand trends and high-value products
* Process Improvement — Optimize procurement planning and reduce financial loss

## 📁 Datasets Used

The following datasets were used for core analysis:

SalesFINAL12312016.csv
→ Customer sales transactions and revenue data

PurchasesFINAL12312016.csv
→ Procurement and supplier delivery data

BegInvFINAL12312016.csv & EndInvFINAL12312016.csv
→ Inventory stock levels at the beginning and end of the period

(Other datasets were provided but core optimization tasks were achieved using these primary sources.)

## 🔍 Analysis Performed

### 1. Demand Forecasting (Time Series Analysis)
Sales data was aggregated into daily demand patterns and analyzed using a 7-day moving average model.

#### Key Findings:
* January showed strong demand with multiple high-volume sales peaks
* February experienced a noticeable drop in sales volume
* Short-term forecasting highlighted a downward demand trend

#### Business Impact:
* Helps align purchase planning with real demand
* Prevents over-ordering during low demand periods
* Supports data-driven stock planning

  ### 2. ABC Inventory Classification

  Products were classified based on revenue contribution:
```
| Category | Product Count | Business Meaning                |
| -------- | ------------- | ------------------------------- |
| A        | 36,801        | High-value, priority products   |
| B        | 48,205        | Medium importance products      |
| C        | 85,125        | Low-value, slow-moving products |
```
#### Key Insight:
A small percentage of products generate the majority of revenue, while a large number of products contribute very little.

#### Business Impact:
* Focus inventory investment on A-category products
* Reduce excess stock of C-category products
* Optimize warehouse space and working capital

### 3. Lead Time Analysis (Procurement Efficiency)

Supplier delivery performance was analyzed using:
```
Lead Time = Receiving Date − Purchase Order Date
```
#### Result: Average Lead Time ≈ 7.6 days

#### Business Impact:
* Helps procurement teams plan orders in advance
* Reduces stockout risk
* Improves supplier performance evaluation

### 4. Reorder Point Calculation (Stock Replenishment Strategy)

Reorder point was calculated using:
```
Reorder Point = Average Daily Demand × Average Lead Time
```
#### Results:
* Average Daily Demand ≈ 40,852 units
* Reorder Point ≈ 311,328 units

#### Business Meaning:
When inventory reaches approximately 3.1 lakh units, a new purchase order should be placed to ensure continuous stock availability.
This prevents:
* Stock shortages
* Lost sales revenue
* Customer dissatisfaction

### 5. Inventory Turnover Analysis

Inventory movement efficiency was measured using:
```
Inventory Turnover = Total Sales Quantity / Average Inventory
```
#### Result: Inventory Turnover Ratio ≈ 0.53

#### Interpretation:
* Inventory movement is slow
* Overstocking risk exists
* Capital is locked in unsold stock

#### Business Recommendation:
* Reduce slow-moving products
* Improve stock rotation
* Align purchases with demand forecasts

## Key Business Insights Summary

✔ Demand is seasonal and fluctuates significantly
✔ Overstocking risk is present due to low inventory turnover
✔ High-value products require priority stock management
✔ Supplier lead time directly impacts reorder planning
✔ Data-driven reorder strategy reduces stockout and financial loss

## ⚙ Tools & Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Jupyter Notebook

## How To Run This Project Locally

#### Step 1: Install Requirements
Install Anaconda (recommended) or Python 3.8+

#### Step 2: Clone Repository
```
git clone https://github.com/Megha-S-K/Slooze.git
```

#### Step 3: Place Dataset Files
Copy all CSV dataset files into the project directory.

#### Step 4: Open Notebook
Launch Jupyter Notebook and open:
```
inventory_analysis.ipynb
```

#### Step 5: Run All Cells
Run all cells from top to bottom to reproduce analysis and visualizations.

## 📌 Project Highlights

* Handled over 1 million+ sales records
* Built complete analytics pipeline from raw data to business insights
* Applied real-world inventory management techniques
* Generated actionable operational recommendations

## 🏁 Conclusion

This project demonstrates how data science can improve retail inventory efficiency by forecasting demand, prioritizing high-value products, optimizing reorder strategies, and identifying procurement bottlenecks. The analysis provides a scalable framework for intelligent inventory decision-making in real production environments.
* 
