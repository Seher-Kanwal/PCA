# PCA
![image](https://user-images.githubusercontent.com/92606737/230544858-58af4930-48c5-401c-93e5-ca1715c0bca7.png)

Principal Component Analysis (PCA) is a popular unsupervised machine learning technique used for dimensionality reduction. It is used to transform high-dimensional data into a lower-dimensional space while retaining as much of the original information as possible.

PCA works by identifying the directions of greatest variance in the data, and then projecting the data onto these new dimensions. The first principal component is the direction of greatest variance, the second principal component is the direction of second-greatest variance, and so on. Each principal component is orthogonal (i.e., perpendicular) to all the others.

PCA is commonly used in a variety of applications, such as image processing, speech recognition, and bioinformatics. It is especially useful for reducing the dimensionality of large datasets, which can improve the speed and accuracy of many machine learning algorithms.

# Steps

The general steps involved in performing PCA are as follows:

### Standardize the data:

The first step in PCA is to standardize the data by subtracting the mean of each variable and dividing by its standard deviation. This ensures that all variables have the same scale and that no variable dominates the analysis simply because it has a larger magnitude.

### Compute the covariance matrix: 

The next step is to compute the covariance matrix of the standardized data. The covariance matrix is a square matrix that shows how much two variables vary together. The (i,j)th element of the covariance matrix is the covariance between the ith and jth variables, and it is given by:

cov(Xi, Xj) = E[(Xi - E[Xi])(Xj - E[Xj])]

where E[] denotes the expected value operator. If Xi and Xj are positively correlated, then their covariance will be positive; if they are negatively correlated, then their covariance will be negative; and if they are uncorrelated, then their covariance will be zero.

### Compute the eigenvectors and eigenvalues of the covariance matrix: 

The next step is to compute the eigenvectors and eigenvalues of the covariance matrix. An eigenvector of a matrix A is a non-zero vector v such that Av = λv, where λ is a scalar known as the eigenvalue. The eigenvectors and eigenvalues of the covariance matrix are important because they tell us in which direction the data varies the most and how much it varies in that direction.

### Choose the principal components: 
The next step is to choose the principal components based on the eigenvalues. The first principal component is the eigenvector that corresponds to the largest eigenvalue, the second principal component is the eigenvector that corresponds to the second-largest eigenvalue, and so on. The eigenvalues tell us how much variance is captured by each principal component, and we typically choose the top k principal components that capture a large percentage of the total variance (e.g., 95%).

Transform the data: The final step is to transform the original data into the new coordinate system defined by the chosen principal components. This is done by taking the dot product of the original data matrix X with the matrix of eigenvectors V that correspond to the chosen principal components. The transformed data matrix Y is given by:

Y = X V

where Y is a matrix with the same number of rows as X and k columns (where k is the number of chosen principal components).



In summary, PCA works by identifying the directions of greatest variance in the data, and then projecting the data onto these new dimensions. The key mathematical concepts involved in PCA are the covariance matrix, eigenvectors, and eigenvalues. By choosing the top k principal components, we can reduce the dimensionality of the data while retaining most of the information.
