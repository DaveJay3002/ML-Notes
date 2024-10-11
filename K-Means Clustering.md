**K-Means Clustering** is an unsupervised machine learning algorithm used to partition a dataset into **K distinct clusters** based on feature similarity. It aims to group similar data points together while ensuring that data points in different clusters are as dissimilar as possible.

### Key Characteristics of K-Means Clustering:

1. **Centroid-Based**:
    
    - The algorithm identifies **K centroids** (central points) that represent the center of each cluster. Each cluster is formed around these centroids.
2. **Iterative Process**:
    
    - The K-Means algorithm follows an iterative approach:
        1. **Initialization**: Randomly select K initial centroids from the data points.
        2. **Assignment Step**: Assign each data point to the nearest centroid, forming K clusters.
        3. **Update Step**: Recalculate the centroids by taking the mean of all data points assigned to each cluster.
        4. **Convergence**: Repeat the assignment and update steps until the centroids no longer change significantly or a predetermined number of iterations is reached.
3. **Distance Metric**:
    
    - The most common distance metric used is the **Euclidean distance**, which measures the straight-line distance between points in a multidimensional space.

![[Pasted image 20241010180438.png]]

# K-means optimization objective
![[Pasted image 20241010180914.png]]

# Steps of the K-Means Algorithm:

1. **Choose the Number of Clusters (K)**:
    
    - Decide on the number of clusters you want to partition your data into. This is a critical step and can be determined using methods like the Elbow method or Silhouette analysis.
2. **Initialize Centroids**:
    
    - Randomly select K data points from the dataset as the initial centroids (cluster centers). Alternatively, more advanced methods like K-Means++ can be used for better initialization.
3. **Assign Clusters**:
    
    - For each data point in the dataset, calculate the distance to each centroid and assign the data point to the cluster with the nearest centroid. This is usually done using the Euclidean distance formula.
4. **Update Centroids**:
    
    - After all data points have been assigned to clusters, recalculate the centroids of each cluster. The new centroid is the mean (average) of all data points assigned to that cluster.
5. **Check for Convergence**:
    
    - Determine if the centroids have changed significantly since the last iteration. If the centroids do not change (or change very little) or if the maximum number of iterations has been reached, the algorithm has converged. If they have changed, go back to step 3.
6. **Repeat**:
    
    - Continue the assignment and update steps until convergence is reached, resulting in stable centroids and cluster assignments.

### Optional Steps:

- **Post-Processing**:
    
    - After convergence, you may want to analyze the clusters, visualize the results, or further refine the clustering based on domain knowledge.
- **Evaluation**:
    
    - Assess the quality of the clusters using metrics such as inertia (within-cluster sum of squares) or silhouette scores to determine how well the clusters are formed.

# Choosing the right value of K

![[Pasted image 20241010181922.png]]

![[Pasted image 20241010182000.png]]

