# Customer-Segmentation-System

📘 Overview

The Customer Segmentation System is a Machine Learning project that aims to divide customers into different groups (segments) based on their spending behavior and annual income.
This helps organizations and businesses understand their customers more effectively and build targeted marketing strategies.

The project includes data preprocessing, model building using K-Means Clustering, visualization of customer segments, and an interactive Streamlit web application for real-time analysis.

🎯 Objective

The main objective of this project is to:

Identify different types of customers based on income and spending habits.

Help businesses design personalized offers for each segment.

Provide visual insights through an interactive web dashboard.

🧠 Problem Definition

Businesses often deal with large amounts of customer data but fail to interpret it meaningfully.
By applying unsupervised learning, specifically K-Means Clustering, we can automatically group customers with similar purchasing characteristics without predefined labels.

Example:

Cluster 1: High income, high spending customers → “Premium Customers”

Cluster 2: Low income, low spending customers → “Budget Shoppers”

This segmentation improves decision-making in marketing, sales, and customer relationship management.

⚙️ Methodology
1️⃣ Data Collection

Dataset: Mall_Customers.csv
It contains basic customer details such as:

CustomerID

Gender

Age

Annual Income (in thousand dollars)

Spending Score (1–100)

2️⃣ Data Preprocessing

Before training the model:

Checked for null or missing values

Converted categorical features (like Gender) into numeric form

Selected relevant features for clustering — Annual Income and Spending Score

Applied StandardScaler for feature normalization

3️⃣ Model Building

Used K-Means Clustering Algorithm to divide customers into distinct groups.

Steps involved:

Choose the number of clusters (k)

Initialize random centroids

Assign each data point to the nearest centroid

Recalculate centroid positions

Repeat until the centroids stop moving

4️⃣ Finding the Optimal Number of Clusters

Used the Elbow Method:

Plotted the Within-Cluster Sum of Squares (WCSS) against various cluster numbers (k values).

The “elbow point” in the curve indicates the optimal number of clusters (here, k = 5).

5️⃣ Model Training

Applied K-Means with n_clusters = 5.

Trained model identifies 5 unique customer groups.

Saved the model as customer_segmentation_model.pkl using Joblib for deployment.

6️⃣ Visualization

Visualized the clustering results using:

2D Scatter Plots (Income vs Spending Score)

Color-coded clusters to distinguish customer groups

Interactive 3D graphs using Plotly for deeper analysis

These visualizations help understand customer behavior patterns clearly.

7️⃣ Web Application (Deployment)

Created an interactive Streamlit app (customer_app.py) that allows users to:

Input their Annual Income and Spending Score via sliders

Instantly predict the customer’s segment/cluster

View visual representations of customer segments

🖥️ Application Interface

The Streamlit interface enables easy exploration of customer segments and predictions.

⚡ How to Run Locally
Step 1: Clone the Repository
git clone https://github.com/SUBHAM-DEY2005/Customer-Segmentation-System.git
cd Customer-Segmentation-System

Step 2: Install Dependencies
pip install -r requirements.txt

Step 3: Run the Streamlit App
python -m streamlit run customer_app.py


Then open your browser and go to 👉 http://localhost:8501

📈 Output Summary

The model successfully categorized customers into five segments.

The system provides interactive cluster visualization.

Users can input new data to check their predicted segment.

Helps businesses improve customer targeting and marketing efficiency.

🏁 Future Enhancements

Add more customer features like Age, Gender, Occupation

Use advanced clustering (DBSCAN, Hierarchical Clustering)

Build an API backend for data integration

Deploy the app on Streamlit Cloud / HuggingFace Spaces
