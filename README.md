# Anomaly Detection

# Nispera April 2022


## LOGS


### Day 1-2 

- Explored the data, made some insightful graphs to get a better understanding of what is the assignment 
- had a meeting with the client to further discuss the project 


### Day 3 

- cleaned, pivoted and merged all the data frames together 
- tried different clustering models, especially the silhouette model


### Day 4 - 5
 
- DTW ( data time wraping) 
- charting 
- PCA (principle component analysis) for everything and separately 
- different heatmaps
- finding patterns (nacelle, blades pitch)


### Day 8 

- UMAP trying to find different clusters. (no sucess)
- Try PCA with different variations


### Day 10 - 13

- We tried other machine learning models and variation that could give us the desire output
- Try different combinations of variables tyring to find relations among the different variables


### Day 14 - 17

- After a meeting with the company we change the approach 180 degrees, from a ML approach to a statistical one
- We develop a statistical model that was able to spot 2 different anomalies: power curve shift and power curtailment
- We create the following functions
    - Power_cubic_regression. It's a linear regression that takes 2 the wind speed as an input and returns the predicted power generation
    - Sigmoid. The function creates a sigmoid optical curve. We didn't use this to the complexity to implement it. 
    - Power_curve_stats
        - masks
        - Dictionary with different feature engineering objects that we will use
        - Rules for the prediction of Power Curtailments and Power Curve shifts
    - Plot_power_curve
        - Creates the charts for every week
        - Stores the prediction for every week prediction

- Import Data and data management 
- Loops that integrates all the functions, and variables into one model that takes a DF as an input and detects the anomalies 

#### Anomaly detection 
<img src="/images/anomalies_detection_algo.png" width="300" height="300">

### Day 17 -20
- Create the function that would adapt the data frames to be used in a Supervised ML model
- Try different ML models
- Used the K-Nearest Neighbor(KNN) to spot the anomalies. The model had around 90% accuracy

#### Machine Learning Results
<img src="/images/ML_trained_model_results.png" width="700" height="500">

#### KNN model accuracy
<img src="/images/ml_trained_accuracy.png" width="300" height="150">
