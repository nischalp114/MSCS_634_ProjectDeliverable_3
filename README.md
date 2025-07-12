# MSCS_634_ProjectDeliverable_3

Deliverable 3: Classification, Clustering, and Pattern Mining
GROUP MEMBERS:

Name: Nischal Pokharel

Name: Swarna Anjani Devershetty

Name: Vishnu Mallam

Name: Tejeswar Reddy Chemikala

Name: Shyam Nath

Overview

This deliverable focuses on applying classification, clustering, and association rule mining to the Stroke Prediction Dataset. Our goal was to build predictive models, discover natural groupings within the data, and find hidden patterns that could be useful in a healthcare context.

Classification Models

We built two classification models:
Decision Tree
k-Nearest Neighbors (k-NN)

We evaluated the models using confusion matrix, accuracy, F1-score, and ROC curves. We also performed hyperparameter tuning using GridSearchCV to improve performance by testing different values for max_depth in Decision Tree and n_neighbors in k-NN.

Best Scores:

Tuned Decision Tree and k-NN both showed modest performance due to class imbalance, but the Decision Tree provided more interpretable results.

Clustering

We used K-Means clustering with 3 clusters to identify hidden patterns among patients. The data was scaled and reduced using PCA for 2D visualization. The clusters showed distinct groupings based on variables like age, BMI, and glucose level, potentially representing high-risk vs low-risk patient groups.

Association Rule Mining

We applied the Apriori algorithm to find patterns in patient conditions. Continuous variables were binned (e.g., glucose and BMI levels), and we used label encoding to transform categorical data into transaction-style records.

Examples of Discovered Patterns:
Patients who are "old", with "high_glucose" and "has_htn" are often associated with "had_stroke"
Patterns involving combinations of heart disease, smoking status, and BMI also appeared in the top rules.

Key Insights

Classification models need balancing strategies like SMOTE to handle the class imbalance.
Clustering revealed distinct patient profiles that could help in early detection strategies.
Association rules help explain the conditions under which strokes tend to occur, which is valuable for risk modeling and awareness.

Challenges

Class Imbalance: Stroke cases are underrepresented in the dataset, which limited model accuracy.
Mixed Data Types: Needed careful preprocessing and binning for association mining.
Model Tuning: Performance differences between models were small; tuning helped but did not drastically improve scores.

Files Included

Deliverable3.ipynb: Contains all code, model building, tuning, visualizations, and outputs.
README.md: This file summarizing our process, models, results, and challenges.
