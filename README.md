# 🛍️ Customer Shopping Behaviour Analysis

## 📌 Overview
An end-to-end data analytics project that explores retail customer spending habits, subscription trends, discount sensitivity, and customer segmentation. Using **Python**, **MySQL**, and **Power BI**, this project transforms raw transaction data into actionable business insights and an interactive executive dashboard.

---

## 📊 Dataset
* **Records & Features:** 3,900 customer transactions across 18 attributes.
* **Key Columns:** Customer Demographics (`Age`, `Gender`, `Location`), Purchase Details (`Item Purchased`, `Category`, `Purchase Amount (USD)`, `Season`), and Engagement Metrics (`Subscription Status`, `Discount Applied`, `Previous Purchases`, `Review Rating`, `Frequency of Purchases`).

---

## 🛠️ Tools & Technologies
* **Python (`Pandas`, `NumPy`, `Scikit-Learn`, `SQLAlchemy`, `PyMySQL`):** Data cleaning, feature engineering, K-Means clustering.
* **MySQL:** Business intelligence querying using  window functions, and aggregations.
* **Microsoft Power BI:** Interactive data visualization and KPI reporting.

---

## 🔄 Project Steps

### 1. Data Cleaning & Feature Engineering (Python)
* Handled 37 missing values in `Review Rating` using category-wise median imputation.
* Standardized column names to `snake_case` and removed redundant columns (`promo_code_used`).
* Engineered age groups (`Young Adult`, `Adult`, `Middle_aged`, `Senior`) and converted purchase frequencies into numerical day intervals.

### 2. Customer Segmentation (Machine Learning)
* Scaled key behavioral features (`previous_purchases`, `purchase_amount`, `review_rating`) with `RobustScaler`.
* Applied **K-Means Clustering** to group shoppers into 4 distinct customer segments.
* Exported the cleaned dataset directly into a MySQL database (`customer_behaviour`).

### 3. Business Intelligence Analysis (MySQL)
* Wrote 16 SQL queries to analyze revenue by gender, age group, shipping type, and subscription status.
* Identified top-performing products per category and segmented customers into `New`, `Returning`, and `Loyal` tiers.

### 4. Visual Reporting (Power BI)
* Connected Power BI to the MySQL database to build an interactive dashboard tracking revenue, average order value, ratings, and cluster breakdowns.

---

## 📈 Dashboard
PowerBi dashboard is available in file which is uploaded...

---

## 💡 Key Results & Insights
* **Customer Segments (K-Means):**
  * **Cluster 0:** Frequent buyers with moderate spending (~$58) and lower ratings (~3.07) — *opportunity for service improvement*.
  * **Cluster 1:** Highly loyal, repeat buyers (~38 past purchases) with high satisfaction (~4.41 rating) — *ideal VIP retention group*.
  * **Cluster 2:** Low-frequency, lower-spend shoppers (~$37) — *target for onboarding promotions*.
  * **Cluster 3:** High-ticket spenders (~$82 average spend) with growth potential in repeat orders.
* **Subscription & Shipping Impact:** Analyzed spending differences between subscribers vs. non-subscribers and Express vs. Standard shipping users to guide promotional strategies.
* **Discount Dependency:** Identified specific items heavily reliant on discounts to drive sales volume.

