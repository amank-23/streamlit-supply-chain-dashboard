# E-commerce Inventory Optimization & Sales Analysis

<div align="center">

**[<img src="https://static.streamlit.io/badges/streamlit_badge_black_white.svg" alt="Streamlit App" height="30">](https://dashboardpy2311.streamlit.app/)**

</div>

<div align="center">

![Python](https://img.shields.io/badge/python-v3.8+-blue.svg)
![Streamlit](https://img.shields.io/badge/streamlit-v1.0+-red.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter%20Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)

_A comprehensive data science solution for transforming reactive inventory management into proactive, data-driven decision making_

</div>

---

## Project Overview

This project delivers an **end-to-end Analysis** that analyzes historical e-commerce sales data to derive actionable inventory management strategies. By leveraging advanced analytics techniques including ABC analysis, RFM segmentation, and time-series forecasting, this solution enables businesses to transition from reactive to **proactive, data-driven inventory optimization**.

### Key Value Propositions

- **Inventory Prioritization**: Identify which products deserve focused attention and capital allocation
- **Customer Segmentation**: Understand customer value distribution for targeted retention strategies
- **Demand Forecasting**: Predict future sales with quantified uncertainty for optimal safety stock planning
- **Interactive Dashboard**: Present insights through a professional, user-friendly web interface

---

## Live Dashboard Features

<div align="center">

_ Interactive Streamlit Dashboard with 5 Comprehensive Tabs_

</div>

### Tab 1: Dashboard

- **Key Performance Indicators (KPIs)**
- **Monthly Revenue Trends**
- **Business Health Metrics**

### Tab 2: ABC Analysis

- **Product Portfolio Segmentation**
- **Revenue Concentration Visualization**
- **Top Performing Products Table**

### Tab 3: RFM Customer Segmentation

- **Customer Value Distribution**
- **RFM Score Histogram**
- **High-Value Customer Identification**

### Tab 4: Demand Forecasting

- **30-Day Sales Forecast Visualization**
- **Model Performance Metrics**
- **Historical vs. Predicted Trends**

### Tab 5: Project Summary

- **Comprehensive Analysis Overview**
- **Key Business Insights**
- **Model Comparison & Selection Rationale**

---

## Dataset Information

| **Attribute**    | **Details**                                                                                              |
| ---------------- | -------------------------------------------------------------------------------------------------------- |
| **Source**       | [UCI Machine Learning Repository - Online Retail](https://archive.ics.uci.edu/ml/datasets/online+retail) |
| **Records**      | 541,909 transactions                                                                                     |
| **Time Period**  | December 2010 - December 2011                                                                            |
| **Geography**    | UK-based online retailer                                                                                 |
| **Data Quality** | Cleaned dataset: 397,884 valid transactions after preprocessing                                          |

---

## Key Analytical Insights

### 1. Product Performance (ABC Analysis)

**The 80/20 Rule in Action**: Product portfolio demonstrates strong Pareto distribution

| **Category** | **Products**           | **Revenue Share** | **Strategic Focus**              |
| ------------ | ---------------------- | ----------------- | -------------------------------- |
| **Class A**  | 21.1% (849 products)   | 80.0%             | High priority, maximum attention |
| **Class B**  | 15.8% (634 products)   | 15.0%             | Moderate management              |
| **Class C**  | 63.1% (2,536 products) | 5.0%              | Minimal oversight required       |

** Business Impact**: Focus 80% of inventory capital and warehouse space on just 849 high-value Class A products.

---

### 2. Customer Value (RFM Segmentation)

**Customer concentration is even more pronounced than product concentration**

| **Customer Segment**            | **Percentage** | **Revenue Contribution** | **Action Required**    |
| ------------------------------- | -------------- | ------------------------ | ---------------------- |
| **Best Customers (RFM=12)**     | 11.3%          | 49.8%                    | VIP retention programs |
| **Good Customers (RFM=9-11)**   | 28.7%          | 35.2%                    | Loyalty incentives     |
| **Regular Customers (RFM=6-8)** | 45.0%          | 12.5%                    | Engagement campaigns   |
| **At-Risk Customers (RFM<6)**   | 15.0%          | 2.5%                     | Win-back strategies    |

** Business Impact**: Implement targeted loyalty programs for the top 11.3% of customers who drive nearly half of all revenue.

---

### 3. Demand Forecasting Model Comparison

**Rigorous model validation ensures reliable predictions for inventory planning**

#### Model Performance Comparison

| **Model**                 | **MAE (Units)** | **Relative Performance** | **Model Complexity**     |
| ------------------------- | --------------- | ------------------------ | ------------------------ |
| **Exponential Smoothing** | **20.68**       | **Best**                 | Simple, interpretable    |
| **XGBoost Regressor**     | ~24.15          | Moderate                 | Complex, requires tuning |
| **Naive Forecast**        | 32.10           | Poor                     | Overly simplistic        |
| **Mean Forecast**         | 24.48           | Poor                     | No trend awareness       |

#### Why Exponential Smoothing (MAE: 20.68) Was Selected

** Superior Performance**:

- **35% better** than naive forecasting (32.10 vs 20.68)
- **16% better** than mean forecasting (24.48 vs 20.68)
- **14% better** than complex XGBoost model

** Practical Advantages**:

- **Interpretable**: Business stakeholders can understand the model logic
- **Fast Training**: Minimal computational requirements
- **Robust**: Handles seasonality and trends effectively for retail data
- **Production-Ready**: Easy to deploy and maintain

** Business Translation**:
_"On average, our daily forecast will be off by ±20.68 units, enabling precise safety stock calculations and optimal inventory levels"_

---

## Technical Architecture

### Technology Stack

| **Layer**            | **Technology**              | **Purpose**                     |
| -------------------- | --------------------------- | ------------------------------- |
| **Data Processing**  | Pandas, NumPy               | Data manipulation and analysis  |
| **Visualization**    | Matplotlib, Seaborn, Plotly | Static and interactive charts   |
| **Forecasting**      | Statsmodels                 | Time-series modeling            |
| **Machine Learning** | Scikit-learn, XGBoost       | Model comparison and validation |
| **Web Interface**    | Streamlit                   | Interactive dashboard           |
| **Data Storage**     | Excel/CSV                   | Lightweight data persistence    |

### Project Structure

```
ecommerce_inventory_optimization/
├── 📁 data/
│   └── Online Retail.xlsx          # Raw dataset
├── 📁 src/
│   ├── dashboard.py                # Main Streamlit application
├── 📁 notebooks/
│   └── sprint_analysis.ipynb      # Detailed analysis & model
├── 📄 README.md                   # Project documentation

```

---

## Quick Start Guide

### Prerequisites

- Python 3.8 or higher
- 8GB RAM recommended
- Modern web browser

### Installation & Launch

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd ecommerce_inventory_optimization
   ```

2. **Create virtual environment** (recommended)

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install pandas numpy openpyxl matplotlib seaborn statsmodels streamlit plotly
   ```

4. **Launch the dashboard**

   ```bash
   streamlit run src/dashboard.py
   ```

5. **Access the application**
   - The dashboard will automatically open in your default browser
   - URL: `http://localhost:8501`

---

## Business Impact & ROI

### Quantifiable Benefits

| **Optimization Area**      | **Potential Impact**                        | **Implementation**           |
| -------------------------- | ------------------------------------------- | ---------------------------- |
| **Inventory Capital**      | 20-30% reduction in tied-up capital         | Focus on Class A products    |
| **Stockouts**              | 15-25% reduction in lost sales              | Forecast-driven safety stock |
| **Customer Retention**     | 10-15% increase in customer lifetime value  | Targeted RFM programs        |
| **Operational Efficiency** | 30-40% reduction in manual forecasting time | Automated demand prediction  |

---

## Future Enhancements

- [ ] **Real-time Data Integration**: Connect to live e-commerce APIs
- [ ] **Advanced ML Models**: Implement deep learning for complex seasonality
- [ ] **Multi-product Forecasting**: Extend forecasting to entire product portfolio
- [ ] **Automated Alerting**: Email notifications for inventory thresholds
- [ ] **Mobile Dashboard**: Responsive design for mobile access
- [ ] **A/B Testing Framework**: Compare inventory strategies systematically

---
