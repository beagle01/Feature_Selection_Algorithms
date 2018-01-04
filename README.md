# Feature_Selection_Algorithms

1. Feature selection: univariate selection. Pearson correlation is only for linear relationship of two variables.  

2. Mutual information and maximal information coefficient (MIC)  
  
3. Model Based Ranking: Linear Regression, Lasso, and Random Forest regressor.  Use coefficient of regression models for selecting and interpreting features.  This approach can work well when the data is not very noisy and the features are independent.   
  
   Regularization is a method for adding additional constraints or penalty to a model with the goal of preventing overfitting and improving generalization. L1 regularization / Lasso (Linear model trained with L1 prior as regularizer) solves the minimization of the least-squares penalty. L2 regularization / Ridge (or Tikhomov regularization) solves a regression model where the loss function is the linear least squares function and regularizaion is given by the L2-norm.  
   Random forests are among the most popular machine learning methods thanks to their relatively good accuracy, robustness and ease for use. Random forests are popular approaches for feature ranking. They provide two straightforward methods for feature selection: mean decrease impurity and mean decrease accuracy. Mean decrease impurity: Gini impurity or informatio gain/entropy for classification, variance for regression trees. Mean decrease accuracy is used to directly measure the impact of each feature on accuracy of the model, to permute the values of each feature and to measure how much the permutation decreases the accuracy of the model.   
  
4. Stability Seletion and Recursive Feature Elimination (RFE). Both can be considered wrapper methods. They build on top of other (model based) selectin methods such as regression or SVM, building models on different subsets of data and extracting the ranking from the aggregates. Stability selection is based on subsampling in combination with selection algorithm (which could be regression, SVMs or other similar method).  
  
   Stability selection is useful for both pure feature selection to reduce overfitting and data interpretaton: in general, good features won't get 0 as coefficients because there are similar, correlated features in the dataset.  
   Recursive feature elimination (RFE) is based on the idea to repeatedly construct a model (for example an SVM or a regression model) and to choose either the best or worst performing feature (for example based on coefficients), setting the feature aside and then repeating the process with the rest of the features.This process is applied until all features in the dataset are exhausted. Features are then ranked according to when they were eliminated. So it is a greedy optimization for finding the best performing subset of features.  
