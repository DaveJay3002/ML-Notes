A **Decision Tree** is a supervised machine learning algorithm used for both classification and regression tasks. It models decisions in the form of a tree-like structure, where each internal node represents a feature or attribute, each branch represents a decision rule, and each leaf node represents an outcome or class label.
[[Entropy]] [[Information Gain]] [[One-hot encoding]] [[Continuous Features]] [[Regression Trees]] 
[[Ensemble Trees]] [[Random Forest]] [[XGBoost]]
### Key Characteristics:

- **Root Node**: Represents the entire dataset and is split into sub-nodes based on the feature that best divides the data.
- **Internal Nodes**: Represent conditions or features on which the data is split.
- **Leaf Nodes**: Represent the final decision or output.

![[Pasted image 20241010144014.png]]

# Decision Tree Learning
![[Pasted image 20241010144200.png]]

### How to choose what feature to split on at each node?
The feature that has the most purity that is if it classifies it with highest accuracy.
But that is generally not the case so we want the best feature to split first and the less important features later in the tree.

### When do you stop splitting?
When a node is 100% one class
When splitting a node will result in the tree exceeding a maximum depth
When improvements in purity score are below a threshold
when number of examples in a node is below a threshold

# Steps for Decision Trees
- Start with all examples at the root node
- Calculate information gain for all possible features, and pick the one with the highest information gain.
- Split the dataset according to selected feature, and create left and right branches of the tree
- Keep repeating the splitting process until stopping criteria is met:
	- When a not is 100% one class
	- When splitting a node will result in the tree exceeding a maximum depth
	- Information gain from additional splits exceeding a maximum depth 
	- Information gain from additional splits is less than threshold
	- When number of examples in a node is below a threshold
 
# When to use decision trees
![[Pasted image 20241010152717.png]]