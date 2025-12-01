# Customer-Segmentation-for-Targeted-Marketing

This project performs customer segmentation using machine learning to help businesses identify distinct customer groups based on demographic, behavioral, and transaction records. The process involves data cleaning, exploratory data analysis (EDA), feature scaling, clustering using K-Means, visualization with PCA, and generation of actionable insights.

📌 Project Overview

Businesses often manage thousands of customer profiles with diverse purchase behaviors. Understanding these patterns helps in:

✔ Tailored marketing campaigns

✔ Product recommendation strategies

✔ Personalized communication

✔ Improved customer retention


This notebook processes the dataset and automatically generates clusters that represent different types of customers based on their attributes.

🛠 Tech Stack
Category	Technologies
Programming	Python
Data Handling	Pandas, NumPy
ML & Scaling	Scikit-Learn (KMeans, PCA, StandardScaler)
Visualization	Matplotlib, Seaborn
🔄 Workflow / Pipeline

1️⃣ Import Libraries

The libraries required for data processing, visualization, and clustering algorithms are loaded.

2️⃣ Load Dataset

The CSV dataset (customer_segmentation_data.csv) is loaded into a pandas DataFrame and its shape & preview are displayed.

3️⃣ Exploratory Data Analysis (EDA)

We inspect:

Data types

Missing values

Summary statistics

Duplicates

This helps us understand dataset structure and quality.

4️⃣ Data Cleaning

Performed in two parts:

Numerical features → missing values filled with median

Categorical features → missing values filled with mode

Duplicate rows removed

This step ensures that clustering is not affected by inconsistent or incomplete data.

5️⃣ Feature Selection

Only numeric features are used for clustering, as K-Means operates on numerical values. We extract meaningful attributes that contribute to segmentation.

6️⃣ Feature Scaling

StandardScaler standardizes the dataset to ensure all features contribute equally.
This prevents high-magnitude features from dominating the clustering output.

7️⃣ Determine Optimal Number of Clusters (K)

Two evaluation techniques are implemented:

Elbow Method — identifies minimum within-cluster variance (WCSS)

Silhouette Score — measures clustering quality

Both graphs guide the selection of the best K value.

8️⃣ Apply K-Means Clustering

Once the best value of K is chosen, K-Means is executed and each customer is assigned a cluster label.

9️⃣ PCA 2D Visualization

Since high-dimensional data cannot be plotted directly, PCA reduces features to 2 dimensions for visualization.
A scatter plot displays:

Cluster boundaries

Separation between segments

🔟 Cluster Profiling

Essential for business insights — calculates the average value of each feature per cluster.
This helps interpret and describe customer personas (e.g., high spenders, price-sensitive buyers, frequent shoppers).

1️⃣1️⃣ Export Results

The labeled dataset with Cluster column is exported as:

customer_segments_output.csv


This file can be used for dashboards, Power BI, CRM uploads, or marketing campaign design.

📊 Example Use Cases
Business Area	Impact
Marketing	Targeted campaigns by segment
Sales	Personalized offers for high-value groups
Product Strategy	Identify category preferences
Customer Experience	Improve retention & loyalty
🚀 How to Run the Notebook

Upload the dataset: customer_segmentation_data.csv

Install required packages (if missing):

pip install pandas numpy matplotlib seaborn scikit-learn


Run the notebook cells in order

View generated segmentation visualizations and export file

📁 Output Files Generated
File	Description
customer_segments_output.csv	Original dataset + cluster labels
PCA visualization	2D plot of customer groups
Cluster profiling	Table of mean feature values per group

📌 Next Improvements (Optional)

Potential add-ons for future project expansion:

🔹 Use DBSCAN or Gaussian Mixture Models for comparison

🔹 Build customer personas report automatically

🔹 Deploy as Streamlit / Flask web app

🔹 Build dashboard in Power BI or Tableau

⭐ Contribution

Feel free to fork this repo and submit pull requests to enhance segmentation logic, visualizations, or usability.

📝 License

This project is licensed under the MIT License — free to use and modify.
