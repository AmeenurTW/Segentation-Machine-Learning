# 📊 Data-Driven Customer Segmentation with K-Means Clustering

### 👨‍💻 Author  
**Ameenurrahman Tohwae**  
Machine Learning Project — 20 July 2025  
Student ID: 651437005

---

## 📝 Project Objective

This project applies **K-Means Clustering** to perform customer segmentation on mall customer data.  
The main goal is to group customers based on **Annual Income** and **Spending Score**, enabling businesses to better understand their customers and apply targeted marketing strategies.

---

## 🎯 Why Customer Segmentation?

- Customers behave differently based on income and purchasing habits.
- Understanding those differences allows businesses to:
  - Offer targeted promotions
  - Allocate marketing budget efficiently
  - Build customer loyalty and retention

---

## 🤖 Why K-Means Clustering?

| ✅ Reason | Explanation |
|----------|-------------|
| Easy to implement | Simple algorithm with fast results |
| Works well with 2D data | This dataset uses only Income and Spending Score |
| Unsupervised learning | Suitable for unlabeled data |
| Interpretable results | Clusters are easy to visualize and explain |
| Flexible K | Elbow Method helps us determine optimal number of clusters |

> 📘 *K-Means is a partition-based clustering algorithm that minimizes intra-cluster variance (inertia) by assigning points to the nearest centroid.*

---

## 📚 Dataset Description

- 📦 Source: [Kaggle – Mall Customers Dataset](https://www.kaggle.com/vjchoudhary7/customer-segmentation-tutorial)
- 🧾 Records: 200 customers
- 🧮 Features:
  - `CustomerID`
  - `Gender` (converted to numeric)
  - `Age`
  - `Annual Income (k$)`
  - `Spending Score (1–100)`

---

## 🧠 What is Spending Score (1–100)?

**Spending Score** is a score assigned by the mall based on customer purchasing behavior, such as:
- Frequency of purchases
- Purchase amount
- Recency
- Loyalty

> The score ranges from **1 (low spending)** to **100 (high spending)**.

| Score Range | Description        | Behavior                |
|-------------|--------------------|--------------------------|
| 0–20        | Very low spender   | Rarely shops             |
| 21–40       | Low spender        | Occasionally shops       |
| 41–60       | Average spender    | Shops moderately         |
| 61–80       | High spender       | Frequent, regular shopper |
| 81–100      | Very high spender  | Premium / loyal customer |

**Why 1–100?**
- ✅ Easy to interpret (like test scores)
- ✅ Makes comparisons between customers simple
- ✅ Suitable scale for clustering with variance
- ✅ Helps distinguish customer types clearly

---

## ⚙️ Project Workflow

1. **Data Cleaning**
   - Removed `CustomerID`
   - Converted `Gender` to numeric
   - Checked for missing values

2. **Feature Selection**
   - Selected: `Annual Income`, `Spending Score`

3. **Data Scaling**
   - Applied `StandardScaler` to normalize values

4. **Elbow Method for Optimal K**
   - K = 5 gives best balance between accuracy and simplicity

5. **K-Means Clustering**
   - Model trained with `n_clusters=5`
   - Clusters assigned to customers

6. **Analysis & Visualization**
   - Cluster profiling by mean income & score
   - 2D scatter plot for cluster visualization

---

## 📈 Elbow Method

> The Elbow Method suggests that **K = 5** is optimal as the "inertia" drops significantly before flattening out.

![Elbow Plot](./images/elbow.png)

---

## 🧩 Cluster Profiles

| Cluster | Avg Income | Avg Score | Description                |
|--------:|-----------:|-----------:|----------------------------|
| 0       | 25.7       | 79.3       | Low income, high spending → Loyal low-income |
| 1       | 88.2       | 17.1       | High income, low spending → Under-engaged |
| 2       | 86.5       | 82.1       | High income, high spending → Premium 💎 |
| 3       | 26.3       | 20.9       | Low income, low spending → Less relevant |
| 4       | 55.3       | 49.5       | Average income/spending → Balanced |

---

## 🖼️ Final Cluster Visualization

> This 2D scatter plot shows customer distribution across 5 clusters.

![Cluster Plot](./images/cluster_plot.png)

---

## 💡 Business Insights

- **Group 2**: High-value customers → Focus on loyalty, exclusivity
- **Group 1**: Wealthy but inactive → Reactivate via offers/incentives
- **Group 0**: Low-income, high usage → Support with loyalty points
- **Group 3**: Possibly cost-ineffective to target
- **Group 4**: Neutral → Potential for conversion

---

## 🧾 Conclusion

K-Means successfully segmented customers into meaningful groups based on income and spending.  
This allows businesses to move from "one-size-fits-all" marketing to **data-driven personalized strategies**.

---

## 📁 Folder Structure

---

## 📌 Future Improvements

- Try other clustering methods (e.g., DBSCAN, Agglomerative)
- Add more features (Age, Gender)
- Connect with Recommendation System

---

> ✨ *Project by Ameenurrahman Tohwae — Fatoni University*  
> 🔗 Contact: nxqmee064@gmail.com
