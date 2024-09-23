**K-Means** is an unsupervised machine learning algorithm used for **clustering** data into distinct groups (clusters) based on similarity. It partitions the data into **K** clusters, where each data point belongs to the cluster with the nearest mean.

### How K-Means Works:

1. **Initialization**:
   - Choose the number of clusters (**K**).
   - Randomly initialize **K centroids** (cluster centers) within the data space.

2. **Assignment**:
   - For each data point, calculate the **Euclidean distance** between the point and each centroid.
   - Assign the data point to the nearest centroid, forming **K clusters**.

3. **Update**:
   - Recalculate the centroids by computing the **mean** of all the data points assigned to each cluster.
   - Repeat the assignment and update steps until the centroids no longer change or a maximum number of iterations is reached.

4. **Convergence**:
   - The algorithm converges when the centroids stabilize (i.e., no longer shift significantly), meaning that the clusters are final.

### Key Points:
- **K** is predefined, meaning the number of clusters must be chosen before running the algorithm.
- The distance metric used is typically **Euclidean distance**, but others can be used based on the application.
- The result depends on the initial placement of centroids, so running K-Means multiple times with different initializations can help improve results (using techniques like **K-Means++** initialization).

### Advantages:
- Simple and easy to implement.
- Works well with large datasets.
- Efficient when K and the number of features are not too large.

### Disadvantages:
- Sensitive to the choice of K (the number of clusters).
- May converge to a local minimum, meaning the clustering can be suboptimal.
- Does not handle clusters of non-convex shapes or varying sizes well.

### Use Cases:
- **Customer segmentation**.
- **Image compression**.
- **Anomaly detection**.

This code will cluster the data into 3 clusters, with labels assigned to each data point and centroids updated iteratively.