# Online Shoppers Behaviour Clustering (MLDM)

This repository contains an unsupervised machine learning project that I developed to explore behavioural patterns in online shopping sessions using clustering techniques.

In this project, I worked with the **Online Shoppers Purchasing Intention Dataset** from the UCI Machine Learning Repository and applied clustering techniques to explore patterns in online shopper behaviour. The focus of the project was not only on applying clustering algorithms, but also on building a clear, reproducible analytical workflow and translating technical results into meaningful business insights for e-commerce decision-making.

## Project Aims

The main aim of this project was to design and implement a complete unsupervised learning pipeline using a real-world behavioural dataset.
**Specifically, I aimed to:**
1. Explore and understand online shopper behaviour through exploratory data analysis (EDA)
2. Prepare mixed numerical and categorical features using robust preprocessing pipelines
3. Apply and compare multiple clustering algorithms
4. Evaluate clustering quality using appropriate internal validation metrics
5. Interpret the resulting clusters in a meaningful and business-relevant way
6. Reflect on ethical and practical considerations when analysing user behaviour data


## Clustering Tasks

Unlike supervised learning problems, this project does not rely on predefined labels. Instead, the task was to identify natural groupings of online shopping sessions based on user behaviour and contextual information.

**The clustering analysis focused on uncovering:**

1. Distinct browsing and engagement patterns among users
2. Differences between high-intent buyers and low-engagement visitors
3. Behavioural groups such as quick-exit users, engaged non-buyers, returning visitors, and high-intent shoppers
4. Although the dataset includes a Revenue variable indicating whether a purchase occurred, this feature was not used during clustering. It was only used after clustering to help interpret and validate the behavioural relevance of the discovered groups.


## Dataset

Source: Online Shoppers Purchasing Intention Dataset

Repository: UCI Machine Learning Repository

Link: https://archive.ics.uci.edu/dataset/502/online+shoppers+purchasing+intention+dataset

Size: 12,330 online shopping sessions


## Features

1. Behavioural features (Administrative, Informational, ProductRelated and their durations)
2. Engagement metrics (BounceRates, ExitRates, PageValues, SpecialDay)
3. Contextual attributes (Month, Browser, OperatingSystems, Region, TrafficType, VisitorType, Weekend)
4. The dataset contains a mix of numerical, categorical and boolean variables, making it well suited for clustering and feature preprocessing experiments.
   

## Methods and Tools
**Clustering Algorithms Used**

**1. K-Means Clustering**
Used as a baseline clustering method due to its simplicity and interpretability.

**2. Gaussian Mixture Models (GMM)**
Used to model clusters probabilistically and capture overlapping behavioural patterns.


## Libraries and Tools

1. Python
2. pandas and numpy for data manipulation
3. matplotlib for visualisation
4. scikit-learn for preprocessing, clustering, evaluation and dimensionality reduction


## Workflow Overview

**The project follows a structured and reproducible workflow:**

1. Loading the dataset directly from a ZIP archive
2. Performing exploratory data analysis (EDA) to understand feature distributions and data quality
3. Handling missing values and correcting data types
4. Building preprocessing pipelines using ColumnTransformer
5. Scaling numerical features and one-hot encoding categorical features
6. Selecting the optimal number of clusters using the Silhouette Score
7. Training K-Means and Gaussian Mixture Models
8. Evaluating cluster quality using internal metrics
9. Visualising clusters using Principal Component Analysis (PCA)
10. Profiling and interpreting clusters for business insights

All plots and summary tables are saved to a structured results directory for reporting.


## Model Evaluation

Because clustering is an unsupervised task, internal validation metrics were used:

1. Silhouette Score – measures how well data points fit within their assigned cluster
2.  Calinski–Harabasz Index – evaluates cluster compactness and separation
3. Davies–Bouldin Index – penalises overlapping clusters

These metrics were used to compare the performance of K-Means and GMM and justify the final model choice.


## Ethical Considerations

Although the dataset is anonymised and publicly available, it represents real user behaviour. Clustering techniques like those used in this project can influence marketing strategies, pricing, and user experience design.

In real-world applications, organisations must:

1. Comply with data protection regulations such as GDPR
2. Avoid manipulative targeting practices
3.  Use behavioural insights responsibly and transparently
4.  Ensure that automated insights support, rather than replace, human decision-making


Ayomide Ogunmakinwa

MSc Data Science

University of Salford
