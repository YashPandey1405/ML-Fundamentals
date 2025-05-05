## 📁 Unsupervised Learning with Python

**Unsupervised Learning** is a type of machine learning where the algorithm is trained on data without labeled responses. The goal is to discover hidden patterns or intrinsic structures in the data. Unlike supervised learning, there is no target variable, and the model tries to group similar data points or reduce the dimensionality of data.

### 📊 Unsupervised Learning Algorithms

In this repository, we implement and demonstrate three widely-used unsupervised learning techniques:

### 1. **K-Means Clustering**:

- A **centroid-based clustering algorithm** that partitions data into **K clusters** by minimizing the variance within each cluster.
- The **Elbow Method** is used with **KneeLocator** to determine the optimal number of clusters.
- Includes:

  - WCSS (Within-Cluster Sum of Squares) plot and Elbow Method using `KneeLocator`
  - Finding the optimal number of clusters
  - Cluster visualization on sample datasets (e.g., Iris)

### 2. **Hierarchical Clustering**:

- Builds a **tree of clusters** by either agglomerating (bottom-up) or dividing (top-down) clusters based on their similarity.
- The algorithm can produce a **dendrogram**, which helps visualize the hierarchy and decide the number of clusters.
- Includes:

  - Dendrogram plotting using `scipy.cluster.hierarchy`
  - Agglomerative clustering
  - Linkage methods like `ward`, `complete`, etc.
  - Visual comparison of clusters

### 3. **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**:

- Groups data based on **density** rather than distance between points.
- It can detect clusters of arbitrary shapes and identify **outliers** (noise points).
- The two key parameters are `eps` (radius of the neighborhood) and `min_samples` (minimum number of points to form a dense region).
- Includes:

  - Usage on non-linear datasets (e.g., `make_moons`)
  - Explanation of `eps` and `min_samples`
  - Noise detection and cluster plotting
