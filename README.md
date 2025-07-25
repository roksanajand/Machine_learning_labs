﻿# Machine_learning_labs

### Titanic – Feature Engineering
This notebook explores feature engineering and missing data handling in the Titanic dataset. It includes identifying variable types, analyzing missing data patterns, and classifying missingness mechanisms (MCAR, MAR, MNAR).

Special attention is given to high-missing-value features such as age, cabin, boat, body, and home.dest. Based on contextual analysis, tailored strategies for handling each type of missing data are proposed (e.g., filling age with median, encoding body status, flagging missing cabin or boat as binary features).

The goal is to improve data quality and prepare meaningful, interpretable features for modeling.

### Titanic – Cardinality
This project focuses on analyzing the cardinality of variables in the Titanic dataset. It involves loading the data, counting unique values per column, and selecting qualitative variables for further processing.

Particular attention is paid to features with high cardinality, such as ticket, cabin, and home.dest, which may cause issues in machine learning models. To address this, the cabin variable was transformed by reducing it to its first letter (indicating the deck), resulting in a 95% reduction in cardinality.

The goal of this transformation is to simplify the dataset, improve interpretability, and prepare it for predictive modeling by minimizing the risk of overfitting.

### Titanic – Data Split
This project demonstrates the process of splitting and preparing the Titanic dataset for machine learning. It starts with loading a cleaned and preprocessed dataset and focuses on selecting a subset of categorical features: 'cabin', its reduced version CabinReduced, and 'sex'.

The data is split into training and testing sets using the train_test_split() function from scikit-learn, with 30% of the data reserved for testing. The cardinality of each feature is analyzed to understand whether the test set contains values that were not present in the training set. This is particularly important for categorical features, as unseen values can reduce model accuracy.

Categorical variables are then encoded into numeric values using custom mapping dictionaries. Missing values are replaced with 0 to ensure compatibility with machine learning models, though it's noted that this might introduce some ambiguity if not handled carefully.

Special attention is paid to the cabin column due to its high cardinality and missing data. The reduced version, CabinReduced, proves to be more stable and suitable for modeling. The entire preprocessing workflow improves the data quality, reduces the risk of overfitting, and prepares the dataset for effective predictive modeling.

### Supervised Learning – Classification
This project explores supervised learning using the Wine dataset. The goal is to classify wine samples into three classes based on chemical attributes. Two models are trained and compared: K-Nearest Neighbors (KNN) and Random Forest.

The workflow includes:

Loading and describing the dataset

Splitting into training and test sets

Applying standardization for distance-based models (KNN)

Training both models and evaluating them using accuracy, precision, recall, F1-score, and confusion matrix

Results show that Random Forest achieves perfect classification, while KNN makes only one mistake. The analysis highlights the importance of data scaling and the differences in model sensitivity to feature distributions.

### Supervised Learning – Regression
This project applies regression techniques to the Boston Housing dataset. The goal is to predict the median value of owner-occupied homes (MEDV) using numerical and categorical features.

The workflow includes:

Data loading and exploratory data analysis (EDA)

Correlation analysis and feature interpretation

Model training using Linear Regression and XGBoost

Hyperparameter tuning with GridSearchCV

Evaluation using MSE, MAE, RMSE, and R²

Results show that XGBoost significantly outperforms linear regression in predictive accuracy. The project also validates regression assumptions (residuals, normality, linearity) and analyzes feature-target relationships.


### Unsupervised Learning – Clustering
This project explores unsupervised learning techniques using the Wine dataset. The aim is to identify natural groupings in the data without using class labels.

The steps include:

Scaling the data using StandardScaler

Applying K-Means and Agglomerative Clustering

Determining the optimal number of clusters using the elbow method

Comparing clustering results with actual class labels using confusion matrix and classification metrics

Visualizing clusters using PCA and scatter plots

The results show that clustering models can partially recover the original class structure, with K-Means achieving good alignment with the true labels after choosing an appropriate number of clusters.




