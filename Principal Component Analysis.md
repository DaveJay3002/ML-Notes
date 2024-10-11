### Principal Component Analysis (PCA)

**Principal Component Analysis (PCA)** is a dimensionality reduction technique used to reduce the number of variables (features) in a dataset while retaining as much variability (information) as possible. It achieves this by transforming the original features into a new set of uncorrelated variables called **principal components**, which are linear combinations of the original variables.

These principal components are ordered in such a way that the first few retain most of the variation present in the original dataset, allowing you to reduce the dimensionality without losing significant information.

---
![[Pasted image 20241011150650.png]] ![[Pasted image 20241011150742.png]]
### Steps of PCA

Here’s a step-by-step explanation of how PCA works:

#### 1. **Standardize the Data (Mean Centering and Scaling)**

- Since PCA is affected by the scale of the variables, it's essential to standardize the dataset so that each feature has a mean of 0 and a standard deviation of 1. This ensures that each feature contributes equally to the analysis.

**Formula for Standardization:**

Xstandard=X−μσX_{\text{standard}} = \frac{X - \mu}{\sigma}Xstandard​=σX−μ​

where XXX is the original feature, μ\muμ is the mean, and σ\sigmaσ is the standard deviation.

#### 2. **Compute the Covariance Matrix**

- The covariance matrix measures how much the variables vary from the mean with respect to each other. This matrix gives insight into the relationships (correlations) between the features.

**Formula for Covariance Matrix**:

Σ=1n−1XTX\Sigma = \frac{1}{n-1} X^T XΣ=n−11​XTX

where XXX is the standardized data matrix, and Σ\SigmaΣ is the covariance matrix.

#### 3. **Compute the Eigenvalues and Eigenvectors of the Covariance Matrix**

- The eigenvectors represent the **principal components** (directions of maximum variance), and the corresponding eigenvalues give the **magnitude** of variance along each principal component.
- Larger eigenvalues indicate principal components that explain more variance.

**Eigenvalue equation**:

Σv=λv\Sigma \mathbf{v} = \lambda \mathbf{v}Σv=λv

where Σ\SigmaΣ is the covariance matrix, λ\lambdaλ are the eigenvalues, and v\mathbf{v}v are the eigenvectors.

#### 4. **Select the Principal Components**

- Rank the eigenvectors (principal components) by their corresponding eigenvalues from highest to lowest. This ranking indicates how much variance each principal component explains.
- Select the top kkk eigenvectors to form the new feature space, where kkk is the number of principal components you want to keep. The first principal component accounts for the most variance, followed by the second, and so on.

#### 5. **Transform the Original Data**

- Project the standardized data onto the new feature space using the top kkk eigenvectors (principal components). This step reduces the dimensionality of the data.

**Transformation formula**:

Xnew=Xstandard⋅VkX_{\text{new}} = X_{\text{standard}} \cdot \mathbf{V}_{k}Xnew​=Xstandard​⋅Vk​

where XnewX_{\text{new}}Xnew​ is the transformed data, and Vk\mathbf{V}_{k}Vk​ is the matrix of the top kkk eigenvectors.

![[Pasted image 20241011151803.png]]

# Reconstruction in PCA
**Reconstruction in Principal Component Analysis (PCA)** refers to the process of approximating the original data from its principal components. Once PCA has been applied to reduce the dimensionality of the data, it is possible to reconstruct an approximation of the original dataset using the selected principal components. This can be useful for understanding how much information is retained after dimensionality reduction and for visualizing the data in the reduced feature space.