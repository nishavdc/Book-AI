# Unsupervised Learning

* The model works on its own to discover information.
* unlabeled data is fed as input.

### Unsupervised learning techniques:

* Dimensionality reduction
  * reduce redundant features
* Density estimation
  * explore data to find some structure within it
* Market basket analysis
* Clustering
  * grouping data points or objects that are similar.

## Clustering

* A cluster is group of data points or objects in a dataset that are similar to other objects in the group, and dissimilar to data points in other clusters.

#### Clustering applications:

![](../.gitbook/assets/image%20%2833%29.png)

![](../.gitbook/assets/image%20%2837%29.png)

#### Clustering Algorithms:

![](../.gitbook/assets/image%20%2834%29.png)

### K-means Clustering

![](../.gitbook/assets/image%20%2858%29.png)

**Algorithm:**

![](../.gitbook/assets/image%20%2853%29.png)

**K-Means Accuracy:**

![](../.gitbook/assets/image%20%2852%29.png)

**Choosing value of K:**

![](../.gitbook/assets/image%20%2844%29.png)

### **Hierarchical Clustering**

* Hierarchical clustering algorithms build a hierarchy of clusters where each node is a cluster consisting of the clusters of its daughter nodes.

![](../.gitbook/assets/image%20%2849%29.png)

#### Agglomerative Algorithm:

![](../.gitbook/assets/image%20%2860%29.png)

#### Distance between clusters:

![](../.gitbook/assets/image%20%2846%29.png)

![](../.gitbook/assets/image%20%2843%29.png)

![](../.gitbook/assets/image%20%2859%29.png)

### Density Based Clustering\(DBSCAN\)

* A density-based clustering algorithm is appropriate to use when examining spatial data.
* The attribute of the DBSCAN algorithm is that it can find out any arbitrary shape cluster without getting affected by noise.
* DBSCAN stands for **D**ensity-**B**ased **S**patial **C**lustering of **A**pplications with **N**oise.
* 
![](../.gitbook/assets/image%20%2855%29.png)

![](../.gitbook/assets/image%20%2847%29.png)

#### How DBSCAN Works:

![](../.gitbook/assets/image%20%2854%29.png)

**Core point**: A data point is a core point if, within R-neighborhood of the point, there are at least M points.

**Border point:** A data point is a BORDER point if:

* Its neighborhood contains less than M data points, or
*  It is reachable from some core point. Here, Reachability means it is within R-distance

**Oulier:**  An outlier is a point that: Is not a core point, and also, is not close enough to be reachable from a core point.

![](../.gitbook/assets/image%20%2841%29.png)

#### Advantages of DBSCAN:

![](../.gitbook/assets/image%20%2861%29.png)

## Recommender Systems

Two types:

* Content based
  * Show me more of the same of what I've liked before.
  * The recommendation in a content-based system is based on user’s tastes, and the content or feature set items.
* Collaborative filtering
  * Tell me what's popular among my neighbors because I might like it too.
  * User based:
    * User-based collaborative filtering is based on the user’s similarity or neighborhood.
  * Item based:
    * Item-based collaborative filtering is based on similarity among items.
  * 

#### **Implementing recommender systems**

* Memory based
  * In memory-based approaches, we use the entire user-item dataset to generate a recommendation systems
* Model based
  * In model-based approaches, a model of users is developed in an attempt to learn their preferences.



