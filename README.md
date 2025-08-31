# 👥 Customer Personality Analysis

A machine learning project analyzing customer data from a **marketing campaign dataset** to understand customer behavior, segment them into clusters, and derive actionable business insights.  

---

## 📂 Project Overview
The main objectives of this project are:
- Clean and preprocess the customer dataset.
- Perform exploratory data analysis (EDA) to identify spending patterns and demographics.
- Apply **K-Means clustering** to segment customers.
- Visualize the characteristics of each cluster.
- Provide marketing and product recommendations for each customer segment.

---

## 📊 Dataset
- **Source:** [Kaggle – Customer Personality Analysis](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)  
- **File Used:** `marketing_campaign.csv`  
- **Rows:** ~2,240  
- **Columns:** 29  

### Key Features:
- **Demographics:** `Age`, `Marital_Status`, `Education`, `Income`, `Kidhome`, `Teenhome`  
- **Spending:** `MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds`  
- **Purchases:** `NumDealsPurchases`, `NumWebPurchases`, `NumCatalogPurchases`, `NumStorePurchases`  
- **Campaigns:** `AcceptedCmp1–5`, `Response`  
- **Target:** Segmentation via clustering  

---

## ⚙️ Technologies Used
- Python 🐍
- Pandas, NumPy (data manipulation)
- Matplotlib, Seaborn (visualization)
- Scikit-learn (clustering)

---

## 🔍 Steps in Analysis
1. **Data Cleaning**  
   - Dropped null values.  
   - Removed outliers (e.g., age > 100, income > 120,000).  
   - Created new features:  
     - `Total_kids = Kidhome + Teenhome`  
     - `Spending = total amount spent across categories`  
     - Re-categorized `Marital_Status` into binary groups (`Married` / `Single`).  

2. **Exploratory Data Analysis (EDA)**  
   - Distribution of marital status.  
   - Scatter plots of **Spending vs Income**.  
   - Campaign acceptance analysis.  

3. **Clustering (K-Means)**  
   - Used the Elbow Method to choose optimal `k`.  
   - Final model: **4 clusters**.  
   - Assigned labels:  
     - Cluster 0 → *Upper Middle Class*  
     - Cluster 1 → *Lower Class*  
     - Cluster 2 → *Upper Class*  
     - Cluster 3 → *Lower Middle Class*  

4. **Visualization of Clusters**  
   - Income, Spending, Age distributions.  
   - Cluster-wise spending patterns across product categories.  
   - Purchasing habits and marketing campaign responses.  

---

## 📈 Results & Insights
- **Upper Class**: Highest income and spending, strong campaign responders.  
- **Lower Class**: Low income, minimal spending, less responsive.  
- **Upper Middle Class**: Moderate income, steady spending, family-oriented.  
- **Lower Middle Class**: Budget-conscious, spend across fewer categories.  
- Marketing strategies can be tailored per cluster (e.g., premium offers for Upper Class, discounts for Lower Class).  

---

## 🚀 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/customer-personality-analysis.git
   cd customer-personality-analysis
2.Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3.Run the Jupyter Notebook
   ``` bash
   jupyter notebook analysis.ipynb
```

## 📌 Future Improvements:
- Apply advanced clustering (DBSCAN, Gaussian Mixture Models).  
- Perform dimensionality reduction (PCA, t-SNE) for better visualization. 
- Build a classification model to predict customer responses. 
- Deploy as an interactive dashboard using Streamlit or Plotly Dash.  
 

---



