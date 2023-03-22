# forecasting-new-product-sales

Prototype a predictive model to forecast the monthly online sales for the first 12 months after the product launches.

# Model Building Approach
* Building a regression model on entire dataset, won’t give optimum results as the sales pattern may vary from product to product.
* Also, since we won’t have historical data for new products, therefore time-series model cannot be built.
* Hypothesis :  “The products that have similar set of features follow the similar sales curve in the initial months of their respective launch”
* To test the above hypothesis, the solution is divided into 3 steps:
    * Clustering
    * Classification
    * Forecasting

* ### Clustering
  * Clusters are created based on the sales pattern of all the products in the training dataset.
  * k-means clustering is used to perform clustering using features Outcome_M[1-12]
  * The optimum number of clusters were validated using Elbow plot & Silhouette method.
  * Optimum number of clusters were identified to be 3 (k=3).

* ### Classification
* Classification model is built to establish a relationship between product features and the clusters created using clustering
* Classification model is built using the product features as input and the cluster variable as target.
* The new products are categorized into one of the clusters using the classification model.
* Built three Classification models using following Algorithms
  * Random Forest (Accuracy = 89.84%)
  * Logistic Regression (Accuracy = 85%)
  * SVM (Accuracy = 87.5
  
* ### Forecasting
* The new products are classified into one of the clusters using Random Forest classification model.
* With product features & the clusters as input, regression model is run to forecast the sales for the first 12 months of product launch.
* Three models were tested:
  * Linear Regression (MAPE = 5.42)
  * Random Forest (MAPE = 0.69)
  * K-nearest neighbors (MAPE = 1.16)

  




