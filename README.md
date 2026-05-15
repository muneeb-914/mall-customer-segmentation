Customer Segmentation Using K-Means Clustering
Task 3 — Arch Technologies Data Science Internship (Month 2)
Name: Muneeb Ur Rehman
Email: mu181842@gmail.com

Objective
Group mall customers into distinct segments based on their purchasing behaviour using K-Means clustering to help the business target each group effectively.

Dataset

Source: Kaggle — Mall Customer Segmentation Dataset
Shape: 200 rows × 5 columns
Columns: CustomerID, Gender, Age, Annual Income (k$), Spending Score (1-100)
Missing Values: None ✅


Step 1 — Data Preprocessing

Renamed columns for simplicity: Annual Income → Income, Spending Score → SpendingScore
Selected features for clustering: Income and SpendingScore
Applied StandardScaler to normalize features to same scale


Step 2 — Finding Optimal K (Elbow Method)

Tested K values from 1 to 10
Plotted inertia vs number of clusters
Elbow point clearly visible at K=5
Selected 5 as optimal number of clusters


Step 3 — K-Means Model Training

Algorithm: K-Means Clustering
n_clusters = 5
n_init = 10
random_state = 42


Step 4 — Cluster Analysis & Visualization

Scatter plot created with 5 distinct colored clusters
Centroids marked with black X markers
Each cluster labeled with business-meaningful name


Customer Segments Identified
ClusterSegment NameAvg IncomeAvg SpendingAvg AgeSize0Average Customers$55k4943811Target Customers ⭐$86k8233392Impulsive Spenders$25k7925223Careful Spenders$88k1741354Budget Customers$26k214523

Key Findings & Business Recommendations
Cluster 1 — Target Customers (High Income, High Spending):
Most valuable segment. 39 customers with $86k income spending freely. Give them VIP treatment, loyalty programs, and premium product access.
Cluster 3 — Careful Spenders (High Income, Low Spending):
Biggest missed opportunity. 35 customers earning $88k but barely spending. Target with luxury campaigns, exclusive offers, and premium experiences to convert them.
Cluster 2 — Impulsive Spenders (Low Income, High Spending):
Young customers (avg 25) spending beyond their means. Offer installment plans, flash sales, and lifestyle-oriented products.
Cluster 0 — Average Customers (Middle Income, Middle Spending):
Largest group (81 customers). Standard marketing approach works here. Focus on consistency and retention.
Cluster 4 — Budget Customers (Low Income, Low Spending):
Price-sensitive segment. Only engage with value deals, discounts, and budget-friendly products.

Conclusion
K-Means successfully identified 5 distinct customer segments. The most actionable insight is Cluster 3 — Careful Spenders — high-income customers not spending represent the biggest revenue growth opportunity for the mall. Targeted premium campaigns for this segment could significantly increase revenue.

Status: TASK 3 ✅ COMPLETE