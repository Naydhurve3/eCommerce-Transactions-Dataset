# Customer Segmentation and Lookalike Model Project
## Project Overview
This project consists of three tasks that aim to analyze customer data, build a lookalike model, and perform customer segmentation using clustering. The data used for this analysis comes from three datasets: Customers.csv, Products.csv, and Transactions.csv. The project is divided into three tasks, each focusing on different aspects of customer data analysis, model development, and clustering. The following is a detailed description of the steps taken to complete each task, including the logic and approach used for the analysis.

## Task 1: EDA and Business Insights
### Objective
Perform Exploratory Data Analysis (EDA) on the provided datasets to uncover patterns and insights that can drive business decisions.

#### Steps:
- `Loading and Inspecting Data`:
The first step was to load the three datasets—Customers.csv, Products.csv, and Transactions.csv—and inspect their structure. This allowed us to understand the columns, data types, and identify any initial issues such as missing values or duplicates.

- `Data Cleaning`:
We checked for missing values and duplicates across all datasets and performed necessary cleaning steps, including removing or filling missing values and handling duplicate rows. This step ensured the data quality was optimal for analysis.

- `Summary Statistics`:
We calculated summary statistics (mean, median, standard deviation) for numerical columns, such as the transaction amounts and customer demographics. This helped understand the central tendency and spread of the data.

- `Exploring Relationships`:
We merged the Customers.csv and Transactions.csv datasets to understand customer behavior across different regions and product categories. This also involved combining Products.csv to analyze sales trends and product popularity.

- `Data Visualization`:
We visualized the data using bar plots, histograms, pie charts, and other plots to highlight key trends, such as:
```
- Sales by region
- Most popular products
- Customer sign-up trends
```
- `Business Insights`:
Based on the EDA, we derived five meaningful business insights:
```
- The most profitable product categories.
- Sales trends across different regions.
- Identification of high-value customers based on spending patterns.
- Most popular product categories by region.
- Customer retention patterns.
```
```
- Deliverables:
Jupyter Notebook: Clean, well-documented code for performing EDA.
PDF Report: A summary of the insights and visuals (maximum 500 words).
```

## Task 2: Lookalike Model
### Objective
Build a lookalike model that identifies similar customers based on their profiles and transaction history, using similarity measures like cosine similarity or Euclidean distance.

#### Steps:
- `Data Preprocessing`:
The first step was to preprocess the data by creating feature vectors for each customer. These vectors were based on transaction behavior (e.g., total spend per product category, purchase frequency) and customer profile details (e.g., region, signup date).

- `Similarity Measurement`:
We used cosine similarity to compute the similarity score between customers. Cosine similarity measures the angle between two vectors and helps quantify how similar two customers are in terms of their transaction behavior and profile.

- `Recommendation System`:
We implemented the model to recommend the top 3 most similar customers for each of the first 20 customers. This recommendation was based on the highest cosine similarity scores.

- `Result Output`:
The results were saved in a file (Lookalike.csv), which included the mapping of the first 20 customers to their top 3 most similar customers.

- `Deliverables`:
```
Lookalike.csv: A file with the top 3 most similar customers for the first 20 customers.
Jupyter Notebook: Document the model development, logic, and recommendation process.
```
## Task 3: Customer Segmentation
### Objective
Perform customer segmentation using clustering techniques based on customer profile and transaction data. Evaluate the clusters using the Davies-Bouldin (DB) Index and other metrics.

#### Steps:
- `Data Preprocessing`:
We began by normalizing and scaling the numerical features to ensure that no single feature dominated the clustering process. This included scaling the transaction data (e.g., total spend, product preferences) and customer demographics.

- `Feature Engineering`:
We engineered additional features to better describe customer behavior, such as the average spend and preferred product categories. This was crucial for capturing the nuances in customer behavior and improving the clustering results.

- `Clustering Algorithm`:
For segmentation, we used the K-Means clustering algorithm, a popular and effective method for partitioning customers into distinct groups based on their similarities. We experimented with different numbers of clusters, ultimately settling on 5 clusters. We evaluated the number of clusters using metrics like the Elbow Method and Silhouette Score.

- `Clustering Evaluation`:
After applying the K-Means algorithm, we evaluated the clustering results using the Davies-Bouldin (DB) Index, which measures the compactness and separation of clusters. The DB Index value for our final model was 4.0076, indicating the degree of separation between clusters. We also computed the Silhouette Score, which was 0.0374, giving an indication of how well-separated the clusters were.

- `Cluster Visualization`:
We used Principal Component Analysis (PCA) for dimensionality reduction to visualize the clusters in 2D. This helped to visually assess the clustering quality and understand the characteristics of each cluster.

- `Final Output`:
```
Number of Clusters: 5
DB Index: 4.0076
Silhouette Score: 0.0374
```
- `Deliverables`:
```
- PDF Report: Document the number of clusters, DB Index value, and cluster insights.
- Jupyter Notebook: Include clustering code, visualizations, and metrics evaluation.

EDA: FirstName_LastName_EDA.pdf, FirstName_LastName_EDA.ipynb
Lookalike Model: FirstName_LastName_Lookalike.csv, FirstName_LastName_Lookalike.ipynb
Clustering: FirstName_LastName_Clustering.pdf, FirstName_LastName_Clustering.ipynb
Upload all files to a public GitHub repository for submission.
```
## Conclusion
This assignment successfully applied various data science techniques, including exploratory data analysis (EDA), a lookalike model, and clustering for customer segmentation. The goal was to uncover patterns and provide business insights, develop a lookalike recommendation system, and segment customers based on their profiles and behaviors. The insights gained from the EDA can help guide business decisions, the lookalike model provides personalized customer recommendations, and the clustering analysis enables better-targeted marketing strategies.
