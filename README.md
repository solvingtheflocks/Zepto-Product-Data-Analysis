# Zepto-Product-Data-Analysis
##  Project Overview
This project performs **data cleaning, exploration, and analysis** on product-level data from the **Zepto grocery platform**. Using SQL, it extracts valuable business insights about pricing, discounts, category revenue, and stock availability to support **data-driven decision-making**.

---

##  Objectives
- Clean and prepare raw data for analysis.
- Explore product information (categories, MRP, discounts, stock levels).
- Generate actionable insights about:
  - High-discount and high-MRP products.
  - Revenue contribution by category.
  - Weight-based product segmentation.
  - Stock-out and discount correlations.

---

##  Files
| File | Description |
|------|--------------|
| `zepto_v2.csv` | Raw dataset containing product details such as price, discount, stock, and category. |
| `Zepto analysis.sql` | SQL script for table creation, data cleaning, and analytical queries. |

---

##  SQL Workflow Summary

### 1. **Data Setup**
```sql
CREATE TABLE zepto (...);
```
Defines the schema with key attributes: `category`, `name`, `mrp`, `discountPercent`, `availableQuantity`, `weightInGms`, and `outOfStock`.

### 2. **Data Exploration**
- Row count and sample preview
- NULL and zero-value checks
- Duplicate product identification
- Stock distribution analysis

### 3. **Data Cleaning**
- Removes products with invalid (`mrp = 0`) values
- Converts price from paise to rupees for consistency

### 4. **Analysis Queries**
| Query | Description |
|-------|--------------|
| Q1 | Top 10 best-value products (highest discounts) |
| Q2 | High-MRP products that are out of stock |
| Q3 | Category-wise estimated revenue |
| Q4 | High MRP but low discount products |
| Q5 | Top 5 categories with highest average discount |
| Q6 | Price per gram for products >100g |
| Q7 | Categorize products as Low, Medium, or Bulk weight |
| Q8 | Total inventory weight per category |

---

## 🧮 Tools Used
- **SQL** (PostgreSQL / MySQL compatible)
- **CSV Data Handling** via DBeaver, pgAdmin, or SQL CLI tools
- **PowwerBi** for dashboard vreation and analysis

---

## 📊 Key Insights
- **Snacks** and **Beverages** show the highest discount ranges.
- High-MRP items (> ₹500) are often out of stock.
- **Personal Care** and **Dairy** contribute heavily to total revenue.
- Most SKUs fall into the **Medium-weight** range (1–5 kg), indicating popular packaging preferences.

## PowerBi Dashboard
<img width="904" height="504" alt="Screenshot 2025-11-30 163556" src="https://github.com/user-attachments/assets/e519402d-e9a4-45e0-8248-38ee9374c6ae" />
