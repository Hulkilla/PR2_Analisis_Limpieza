# Grupal Practise 2 - Data Cleaning and Exploratory Analysis
Subject: M2.851 / Semester: 2024-1 / Date: 06-01-2025

## Authors
1) Marina Fernández Delgado - mfernandezdelg@uoc.edu
2) César Alvarez Mendoza - calvarezmend@uoc.edu


# Real Estate Data Analysis and Modeling

## Project Description
This project involves a comprehensive analysis of the real estate market using structured data and statistical, supervised, and unsupervised methods. The goal is to explore data trends, identify significant patterns, and build reliable predictive models to understand the behavior of property sale prices.

---

## Table of Contents
1. [Data Loading and Cleaning](#data-loading-and-cleaning)
2. [Exploratory Analysis and Transformations](#exploratory-analysis-and-transformations)
3. [Supervised Models](#supervised-models)
4. [Unsupervised Models](#unsupervised-models)
5. [Hypothesis Testing](#hypothesis-testing)
6. [Results and Conclusions](#results-and-conclusions)
---

## Data Loading and Cleaning

The dataset was loaded and cleaned as follows:
- **Individual and Collective Cleaning**: Detection and treatment of missing values, duplicates, and typographical errors.
- **Outlier Removal**: A combination of PCA and Mahalanobis distance was implemented to detect and remove outliers that could distort the analysis.
- **Categorical Variable Transformation**: Converted categorical variables into numerical format using one-hot encoding.

---

## Exploratory Analysis and Transformations

An in-depth analysis of the variables was conducted, including:
- **Trend Analysis**: Visualized relationships between variables (e.g., surface area and sale price, year of construction and sale price).
- **Variable Scaling**: Normalized numerical variables to prevent bias in models.
- **Collinearity Study**: Identified and removed highly correlated variables to reduce redundancy and improve model performance.

---

## Supervised Models

### Models Implemented
- **Linear Regression (LM):**
  - Outcome: Initial R² was low (0.35), indicating limited ability to capture data variability.
  - Improvement: Removed insignificant variables and adjusted hyperparameters.
- **Random Forest:**
  - Optimized model with 1,000 trees and selected significant variables.
  - Outcome: R² = 0.83 and RMSE = 31,784.48.
  - Variable Importance: **Surface area** and the number of **bathrooms** had the most significant impact.

---

## Unsupervised Models

### Models Implemented
- **K-Means Clustering:**
  - Determined the optimal number of clusters using the elbow method (WSS) and silhouette coefficient.
  - Significant clusters: Identified 4 groups with differences in average sale price.
- **DBSCAN (Density-Based Spatial Clustering):**
  - Optimized `eps` and `minPts` parameters.
  - Outcome: Identified 8 clusters, with a substantial number of noise points.
  - Improvement: Adjusted hyperparameters to reduce noise.

---

## Hypothesis Testing

Statistical tests were conducted to analyze the significance of various relationships:
1. **Comparison of price per square meter by property type (house vs. apartment):**
   - Performed a t-test, revealing significant differences between property types.

---

## Results and Conclusions

1. **Key Variables:** **Surface area**, the number of **bathrooms**, and the region (e.g., **Madrid**) are the main determinants of sale price.
2. **Supervised Models:** The **Random Forest** model achieved the best predictive performance (R² = 0.83), highlighting the importance of hyperparameter optimization.
3. **Unsupervised Models:** Clustering using **K-Means** and **DBSCAN** revealed significant groupings, showcasing hidden patterns in the data.
4. **Hypothesis Testing:** Confirmed significant differences across property types.

---

## Requirements
To reproduce this project, install the following R dependencies:
```R
install.packages(c("stringr", "skimr", "dplyr", "ggplot2", "fastDummies", "randomForest", "car", "cluster", "FNN", "dbscan"))
```

## How to Run the Project

1. Clone this repository:
   ```bash
   git clone https://github.com/your_username/real-estate-analysis.git
   ```
2. Open the R script or Markdown file and execute the steps in the specified order.
3. Review the results in the generated visualizations.

---


## License
This project is distributed under the MIT license. See the `LICENSE` file for details.

---

Let me know if you'd like to tweak anything further! 😊
