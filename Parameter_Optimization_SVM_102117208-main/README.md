# Parameter_Optimization_SVM_102117208

This project demonstrates the optimization of Support Vector Machine (SVM) on Electrical Grid Stability Simulated Data obtained from the UCI Machine Learning Repository. 

## Dataset
The Dry Bean dataset consists of 10000 instances, with each instance having 12 features. The dataset is divided into 10 different samples for training and testing.

## Implementation
### Loading the Dataset: 
The dataset is loaded from a CSV file using the pandas library.

### Splitting the Dataset: 
The dataset is split into training and testing sets with a 70-30 ratio, repeated 10 times to get 10 different samples.

### Optimizing SVM: 
SVM is optimized for each sample using cross-validation with 100 iterations. GridSearchCV is used to find the best hyperparameters.

### Recording Results: 
The best parameters and accuracies are recorded for each sample. The sample with maximum accuracy is identified.

<img width="287" alt="image" src="https://github.com/nitish027/Parameter_Optimization_SVM_102117203/assets/142744015/1002f7e8-9ee6-4b6a-9fe7-90b3b1235945">

### Convergence Graph: 
A convergence graph is plotted for the sample with the maximum accuracy, showing how the training and testing accuracies change over iterations during the optimization process.

<img width="628" alt="image" src="https://github.com/nitish027/Parameter_Optimization_SVM_102117203/assets/142744015/3cf8d236-ac94-451f-b63b-3f2b5b40192f">
