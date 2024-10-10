**Random Forest** is an ensemble learning algorithm that constructs multiple decision trees during training and merges their outputs to improve predictive accuracy and control overfitting. It is widely used for both classification and regression tasks.
[[XGBoost]]
### Key Characteristics of Random Forest:

1. **Ensemble Method**:
    
    - Combines the predictions from a large number of decision trees to produce a more accurate and stable prediction.
2. **Bagging (Bootstrap Aggregating)**:
    
    - Uses bootstrapping to create multiple random samples of the training data, allowing each decision tree to be trained on a different subset. This helps to ensure diversity among the trees.
3. **Random Feature Selection**:
    
    - During the training of each decision tree, a random subset of features is selected at each split point. This further enhances diversity and reduces the correlation between the trees, leading to better performance.
4. **Voting/Averaging**:
    
    - For classification tasks, the final output is determined by majority voting among the trees, while for regression tasks, the output is the average of the predictions from all trees.

