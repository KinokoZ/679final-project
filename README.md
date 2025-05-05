# 679final-project

### Note
Due to the large file sizes of the original datasets—eaglei_outages_2014_2023.csv and StormEvents_2014_2024.csv, which together exceed 13GB—we were unable to upload them directly to GitHub. To handle the data efficiently, we utilized Boston University’s SCC (Shared Computing Cluster) to perform all data processing and modeling tasks. For reproducibility, we have included code in our repository and provided links to download the original data.


### Data Download Instructions
Please download the following data and place them into the `eaglei_data/` and `NOAA_StormEvents/` folders:

- [Download eaglei_data]
- [Download NOAA_StormEvents
https://drive.google.com/file/d/15MxvtyyELWtPVDuLospW_b-v6-hXlT-b/view?usp=sharing

full combined dataset
https://drive.google.com/file/d/1u12PBq1QLZQHclc7fXNyNgE-TPXMOseT/view?usp=sharing


###   Abstract
In this project, we develop and evaluate predictive models to estimate the number of affected customers ("customers_day") due to weather-related power outages. Using historical storm event data combined with outage reports, we perform extensive data preprocessing and feature engineering to create a structured dataset suitable for machine learning. We implement four models: Lasso regression, Ridge regression, Random Forest (via ranger), and XGBoost. Among these, XGBoost delivers the best performance, achieving an RMSE of 35.91 and an MAE of 1.26 on the test set. The results demonstrate the effectiveness of ensemble tree-based models in capturing the nonlinear and complex relationships between storm characteristics and outage severity. Our analysis supports the deployment of XGBoost for proactive outage forecasting, helping utility companies and emergency planners better prepare for extreme weather events.

###   Introduction
Power outages caused by severe weather events—such as storms, floods, and hurricanes—can have significant social, economic, and health impacts. Accurate prediction of power outages is essential for utility companies to allocate resources effectively and for emergency response teams to mitigate risk to vulnerable populations. The objective of this study is to develop data-driven models capable of forecasting the number of customers likely to be affected during such events.

We leverage publicly available storm event records and historical power outage data in the U.S. from 2014 to 2023. The raw dataset includes structured and unstructured fields related to the timing, location, type, and magnitude of storm events. A series of preprocessing steps—including missing value imputation, duration calculation, damage normalization, and categorical encoding—are applied to convert the data into a format suitable for machine learning.

To evaluate model performance, we test four predictive algorithms: Lasso (L1-regularized linear regression), Ridge (L2-regularized regression), Random Forest, and XGBoost. We use RMSE, MAE,  MSE and Loss function as the primary evaluation metrics. Our pipeline includes cross-validation for hyperparameter tuning and uses consistent train/test splits to ensure comparability. This report details the modeling workflow and presents insights into model performance, with particular attention to the high accuracy and robustness of the XGBoost model.
