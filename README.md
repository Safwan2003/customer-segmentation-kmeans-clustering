
# **Customer Segmentation using K-Means Clustering** 🚀

## **Overview**
Customer segmentation is a vital technique for improving business strategies. By segmenting customers based on key attributes such as income and spending habits, businesses can tailor their marketing efforts, optimize product recommendations, and increase customer satisfaction. In this project, we used the **K-Means clustering algorithm** to group customers based on their **Annual Income** and **Spending Score**.

---

## **Table of Contents** 📋

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Methodology](#methodology)
   - [Data Preprocessing](#data-preprocessing)
   - [K-Means Clustering](#k-means-clustering)
   - [Model Evaluation](#model-evaluation)
4. [Results](#results)
5. [Conclusion](#conclusion)
6. [LinkedIn Post](#linkedin-post)

---

## **Introduction** 🧠

In the highly competitive world of business, understanding customer behavior is key to improving marketing efforts and driving revenue. This project leverages **K-Means clustering**, a popular unsupervised learning technique, to divide customers into distinct segments based on their **Annual Income** and **Spending Score**. 

### **Key Objectives:**
- **Segmentation of customers** based on their income and spending patterns.
- **Data-driven insights** for businesses to target specific customer groups more effectively.
- **Evaluate the clustering performance** using silhouette scores and visualizations.

---

## **Dataset** 📊

The dataset used in this project is the **Mall_Customers.csv**. This dataset contains information on customers of a mall, including:

| Column Name                | Description                                      |
|----------------------------|--------------------------------------------------|
| **CustomerID**              | Unique identifier for each customer              |
| **Gender**                  | Gender of the customer (Male/Female)             |
| **Age**                     | Age of the customer                              |
| **Annual Income (k$)**      | Annual income of the customer (in thousands)     |
| **Spending Score (1-100)**  | A score representing the customer’s spending habits |

---

## **Methodology** 🔍

### **Data Preprocessing** 🧹

Before applying the clustering model, it’s essential to clean and preprocess the data:

1. **Loading the Data**: The dataset is loaded using **pandas** for further processing.
2. **Encoding Categorical Variables**: The **Gender** column is converted into numeric values using **LabelEncoder**.
3. **Scaling Numerical Features**: Both **Annual Income** and **Spending Score** are scaled using **StandardScaler** to standardize the data, ensuring that both features contribute equally to the clustering process.
4. **Handling Outliers**: Outliers are removed by clipping the values of each column to the 5th and 95th percentiles, ensuring that extreme values don’t skew the results.

---

### **K-Means Clustering** 🧩

The **K-Means clustering** algorithm is a powerful technique for grouping data points into clusters based on similarity. Here's how we applied it to segment the customers:

#### **Step 1: Choosing the Optimal Number of Clusters**

Choosing the right number of clusters is crucial for obtaining meaningful customer segments. To determine the best number of clusters (**k**), we used the **Elbow Method**:

- **Elbow Method**: We plotted the **inertia** (sum of squared distances from each point to its assigned cluster center) against the number of clusters.
- The "elbow" point, where the inertia starts to decrease at a slower rate, suggests the optimal number of clusters. In our case, the optimal **k** was **5**.

#### **Step 2: Applying K-Means**

After determining that **k = 5** is optimal, we ran the K-Means algorithm to segment the customers. The algorithm works by:

1. **Initializing Centroids**: Randomly selecting **k** points in the feature space as initial cluster centers.
2. **Assigning Data Points**: Each customer is assigned to the nearest centroid based on the distance to the center.
3. **Recomputing Centroids**: After all customers have been assigned to clusters, the centroids are recalculated as the mean of all points in each cluster.
4. **Iterating**: The process of assignment and centroid recomputation is repeated until the centroids stabilize (i.e., they no longer change significantly).

#### **Step 3: Cluster Interpretation**

Once the clusters were formed, we examined the characteristics of each customer segment. Each of the 5 clusters represents a distinct group of customers with similar income and spending patterns. Visualizing these clusters helps in understanding the customer profiles:

- **Cluster 1**: High income, low spending.
- **Cluster 2**: Low income, low spending.
- **Cluster 3**: Moderate income, moderate spending.
- **Cluster 4**: High income, high spending.
- **Cluster 5**: Low income, high spending.

These clusters are useful for businesses to develop targeted marketing strategies based on customer characteristics.

---

### **Model Evaluation** ✅

We evaluated the clustering quality using the **Silhouette Score**, which measures how similar each point is to its own cluster compared to other clusters. A higher score indicates well-defined clusters. Our clustering model achieved a silhouette score of **0.55**, indicating reasonably well-defined clusters.

---

## **Results** 📈

### **Elbow Method** 🔔

The **Elbow Method** revealed that the optimal number of clusters is **5**, as indicated by the "elbow" in the plot.

![Elbow Method](images/elbow_method.png)  
*Figure 1: Elbow Method to Determine the Optimal Number of Clusters*

### **Silhouette Score** 🌟

The **Silhouette Score** was calculated to assess the quality of the clusters:

```
Silhouette Score: 0.55
```

This score indicates that the clusters are moderately well-defined.

### **Customer Segments Visualization** 🖼️

The customer segments were visualized using a scatter plot:

- Each cluster is represented by a unique color.
- The **red** points mark the **cluster centroids**, which are the center points of each customer group.

![Customer Segments](images/customer_segments.png)  
*Figure 2: Visualization of Customer Segments*

---

## **Conclusion** 🏁

This project demonstrates the effectiveness of the **K-Means clustering** algorithm in dividing customers into meaningful segments based on their **Annual Income** and **Spending Score**. The results show distinct customer groups that can be targeted for personalized marketing strategies.

By understanding these segments, businesses can:
- Optimize marketing efforts.
- Offer tailored products and services.
- Increase customer satisfaction and retention.

The **5 clusters** we identified represent a diverse range of customer profiles, each with distinct income and spending behaviors. These insights can directly inform marketing campaigns, product offerings, and customer engagement strategies.

---

## **LinkedIn Post** 📢

🚀 Excited to share my latest project on **Customer Segmentation using K-Means Clustering**! 🎉

In this project, I used the K-Means clustering algorithm to segment customers based on their **annual income** and **spending score**. The goal was to identify distinct customer groups to help businesses tailor their marketing strategies.

🔍 **Key Steps**:
1. **Data Preprocessing**: Cleaned the data, handled outliers, and scaled numerical features.
2. **K-Means Clustering**: Applied the Elbow Method to determine the optimal number of clusters.
3. **Model Evaluation**: Evaluated the clusters using the silhouette score.

📊 **Results**:
- The optimal number of clusters was found to be **5**.
- The silhouette score showed that the clusters were **well-defined**.

💡 **Conclusion**:
Customer segmentation is a powerful tool for businesses to understand their customers better and tailor their marketing strategies. This project demonstrates the effectiveness of K-Means clustering in achieving this goal.

Check out the detailed project on my **GitHub**: [GitHub Link](#)

#DataScience #MachineLearning #CustomerSegmentation #KMeansClustering #Python #DataAnalysis

---

This updated version of the `README.md` removes the code section and provides more focus on the details of the **K-Means clustering** process, the evaluation of the clusters, and the resulting customer segments.