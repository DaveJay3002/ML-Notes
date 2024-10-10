**Ensemble Trees** are a class of machine learning algorithms that combine multiple decision trees to improve predictive performance, reduce overfitting, and increase robustness. The basic idea is to leverage the strengths of multiple trees by aggregating their predictions, which often results in better accuracy than individual trees.
[[Random Forest]] [[XGBoost]] 

![[Pasted image 20241010150941.png]]

# Sampling with replacement

**Sampling with Replacement** is a technique used in ensemble tree methods, particularly in the context of **bagging** (Bootstrap Aggregating). This technique involves selecting a subset of data points from the training dataset to train each individual model (or decision tree) in the ensemble. Here’s how it works and why it's important:

### How Sampling with Replacement Works:

1. **Bootstrapping**:
    
    - From the original training dataset, multiple subsets (or "bootstrap samples") are created by randomly selecting data points.
    - When selecting a data point for a new sample, it is possible to choose the same data point more than once (hence "with replacement"). This means some data points may appear multiple times in a single sample, while others may not be included at all.
2. **Creating Multiple Models**:
    
    - Each of these bootstrap samples is used to train a separate decision tree. Since each tree is trained on a different sample of the data, they will learn different aspects of the dataset and potentially capture different patterns.
3. **Aggregation**:
    
    - Once all the trees are trained, their predictions are combined to produce the final output. For regression tasks, the predictions are typically averaged, while for classification tasks, a majority vote is taken.