**Regression Trees** are a type of decision tree specifically designed for predicting continuous target variables. Unlike classification trees that categorize data into distinct classes, regression trees partition the data into subsets that result in the best fit for a continuous output.
[[Variance]] is calculated instead of entropy in regression trees.
### Key Features:

- **Leaf Nodes**: In regression trees, the leaf nodes represent the predicted values of the target variable, usually the mean (or sometimes the median) of the target values in that node.
- **Splitting Criteria**: Instead of using measures like entropy or Gini index (common in classification trees), regression trees use metrics like Mean Squared Error (MSE) to determine the optimal splits.
- **Flexibility**: They can capture complex relationships and interactions in the data without the need for explicit assumptions about the functional form of the relationship.

![[Pasted image 20241010150420.png]]