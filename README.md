

### 🛒 Walmart Sales Data Analysis & Market Basket Analysis

## 📌 Overview

This project presents a comprehensive analysis of Walmart weekly retail sales data using multiple **Data Mining techniques**:

* 📊 Exploratory Data Analysis (EDA)
* 🛒 Market Basket Analysis (Association Rule Mining - Apriori)
* 🔵 K-Means Clustering
* 🌳 Agglomerative Hierarchical Clustering

The goal is to uncover **hidden patterns, customer behavior, and business insights** that can help in decision-making like store layout optimization, promotions, and inventory planning.

---

## 👨‍🎓 Author Details

* **Name:** Abhishek Yaduwanshi
* **Roll No.:** IC-2K22-04
* **Subject:** Data Mining and Warehousing
* **College:** IIPS DAVV, Indore
* **Academic Year:** 2025-26

---

## 📂 Dataset Description

The dataset is derived from Walmart retail data and consists of:

| File              | Records | Description                   |
| ----------------- | ------- | ----------------------------- |
| `train_1k.csv`    | 1000    | Weekly sales data             |
| `features_1k.csv` | 1000    | Economic & environmental data |
| `stores_1k.csv`   | 45      | Store metadata                |
| `test_1k.csv`     | 1000    | Testing dataset               |

---

## 🧾 Features Used

* Store, Dept, Date
* Weekly_Sales
* IsHoliday
* Temperature, Fuel_Price
* MarkDown1–5
* CPI, Unemployment
* Store Type (A/B/C), Size

---

## 🧹 Data Preprocessing

Steps performed:

* Merged datasets (Store + Date)
* Removed duplicate columns & rows
* Filled missing values:

  * MarkDown → 0
  * CPI & Unemployment → Mean
* Converted Date → datetime

✅ Final Dataset:

* Records: **1000**
* Features: **16**
* Missing Values: **0**

---

## 📊 Exploratory Data Analysis (EDA)

### 🔹 Key Insights

* 📈 **Right-skewed sales distribution** → Few high-value outliers
* 🏬 **Store Type A dominates sales**
* 🌡️ **Temperature has weak correlation with sales**
* 💰 Few departments generate majority revenue

---

## 🛒 Market Basket Analysis (Apriori)

### 🔹 Problem Setup

* Transaction = Store + Date
* Items = Departments
* Basket = Departments per store-date

---

### 🔹 Parameters

* `min_support` = 5 transactions
* `min_confidence` = 0.5
* `max_len` = 4
* `lift > 1`

---

### 🔹 Results

* Total Transactions: **74**
* Frequent Itemsets: **4**
* Rules Generated: **10**

---

### 🔹 Sample Rules

| If      | Then    | Confidence | Lift |
| ------- | ------- | ---------- | ---- |
| Dept 2  | Dept 13 | 1.0        | 25   |
| Dept 33 | Dept 83 | 1.0        | 25   |
| Dept 29 | Dept 45 | 1.0        | 25   |

---

### 🔹 Insights

* 💡 Departments strongly co-occur
* 🏪 Useful for:

  * Store layout
  * Cross-selling
  * Product bundling

---

## 🔵 K-Means Clustering

### 🔹 Features Used

* Weekly_Sales
* Temperature
* Fuel Price
* CPI
* Unemployment

---

### 🔹 Optimal Clusters

* Elbow Method → **K = 3**

---

### 🔹 Cluster Interpretation

| Cluster   | Description                  |
| --------- | ---------------------------- |
| Cluster 0 | Average performance          |
| Cluster 1 | High-performing departments  |
| Cluster 2 | Low-performing / weak demand |

---

## 🌳 Agglomerative Clustering

### 🔹 Key Points

* Bottom-up clustering
* No need to predefine K
* Used **Ward linkage**

---

### 🔹 Result

* Dendrogram confirms → **3 clusters**

---

### 🔹 Cluster Meaning

| Cluster   | Insight                      |
| --------- | ---------------------------- |
| Cluster 0 | Normal sales                 |
| Cluster 1 | Low demand (high temp zones) |
| Cluster 2 | High revenue segment         |

---

## ⚖️ K-Means vs Hierarchical

| Feature       | K-Means        | Hierarchical    |
| ------------- | -------------- | --------------- |
| Cluster Count | Predefined     | From dendrogram |
| Approach      | Centroid-based | Bottom-up       |
| Best For      | Large data     | Small data      |

---

## 📈 Key Business Insights

* 🏬 Type A stores generate maximum revenue
* 🛒 Strong product associations exist
* 🌡️ Temperature alone doesn't impact sales significantly
* 💰 High-performing clusters can be targeted for promotions
* 📉 Weak clusters need discounts & strategy

---

## 🚀 Future Improvements

* Use **FP-Growth** for faster association mining
* Apply **DBSCAN** for density-based clustering
* Perform **seasonal trend analysis**
* Scale dataset for better accuracy

---

## 🛠️ Tech Stack

* Python 🐍
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn
* MLxtend (Apriori Algorithm)

---

## 📌 Conclusion

This project successfully applied multiple data mining techniques to extract meaningful insights from Walmart sales data. Both clustering methods validated each other, and association rules revealed strong purchasing patterns.

👉 These insights can directly help in:

* Business strategy
* Marketing optimization
* Inventory management

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and feel free to contribute!

---

