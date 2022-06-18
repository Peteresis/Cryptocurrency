 <p align="center">
 <img src="https://user-images.githubusercontent.com/98360572/174341767-797fc8f8-4899-482e-a72a-c0ad6b9e335c.png" width="100%" height="50%">
</p>

# Module 18 Challenge: Using Unsupervised Learning to Discover Unknown Patterns

Unsupervised learning, also known as unsupervised machine learning, uses machine learning algorithms to analyze and cluster unlabeled datasets. These algorithms discover hidden patterns or data groupings without the need for human intervention. Its ability to discover similarities and differences in information make it the ideal solution for exploratory data analysis, cross-selling strategies, customer segmentation, and image recognition.

This challenge will be using cryptocurrencies data and try to categorize them to build a classification system for new investors. The potential investors are probably lost in cryptocurrency so they will be presented with a report on what cryptocurrencies are on the market and how to categorize them.

---
# :one: Overview of the analysis.

* **Prepocessing of the data**: It is crucial that we preprocess our data before feeding it into our model, as the quality of the data and the relevant information that can be gleaned from it directly influences the model's capacity to learn.  During the preprocessing we need to deal with:
    - Null values
    - Missing values
    - Standardization: transform the values such that the mean of the values is 0 and the standard deviation is 1.
    - Handling Categorical Variables:  Categorical variables are variables that are discrete rather than continuous in nature. For example, an item's color is a discrete variable, while its price is a continuous variable.
* **Use of PCA** (Principal Component Analysis) to reduce the number of dimensions in the analysis.  Principal Component Analysis (PCA) is a well-known unsupervised learning technique for reducing data dimensionality. It improves interpretability while reducing information loss at the same time. It aids in the discovery of the most important features in a dataset and facilitates the charting of data in 2D and 3D. PCA aids in the discovery of a series of linear combinations of variables.
* **Use Elbow Curve**: One of the most important parts of any unsupervised algorithm is figuring out the best number of groups into which the data can be put. One of the most common ways to find this optimal value of k is the "Elbow Method."
* **Use of K-means to cluster data points together**: k-means is a method for grouping data that can be used for unseprvised machine learning. It can sort unlabeled data into a certain number of clusters based on how similar they are. 
* **Visualizing the results with hvplot and Plotly graphic libraries**.

---
# :two: Results.

The complete code of the Jupyter Notebook used for this project can be found here: [Jupyter Notebook Code](https://github.com/Peteresis/Cryptocurrency/blob/5031775b54e064fb16f1cd32dbd73249a24b7640/crypto_clustering.ipynb)

## Screenshots

|   ⚠️ **NOTE: Please click on any image to zoom**     |
| ----------- |

## Preprocessed data for PCA
By using cleaning and preprocessing, the amount of data in the dataset was reduced from `1144 rows x 6 columns` to `532 rows x 4 columns`.
<p align="center">
    <img src="https://user-images.githubusercontent.com/98360572/174353574-54fa1e69-9882-4710-82af-16ca2ece7994.png" width="50%" height="50%">
</p>

## Dataframe with the three principal components

In the table above, each column is a different feature (or dimension) and each different currency produces a different instance (or observation). This sample table, therefore, represents a dataset containing `4` features. However, our actual dataset contains `532` different currencies and therefore `532 x 4 = 2,128 features/dimensions`. These issues would pose a problem for machine learning algorithms, both in terms of computational complexity and the likelihood of over fitting.

To solve this problem, take a closer look at the previous sample table. It seems that currencies with a high value of `TotalCoinsMined` tend to use the same blockchain `ProofType` as well. We could say, for example, that coin `GAP` is representative of all coins using the `PoW/PoS ProofType`, and so we could recommend to similar coins based on this observation.

At a high level, this is what PCA does: it finds typical representations, called principal components, in a high-dimensional dataset so that the dimensions of the original dataset can be reduced while keeping its underlying structure and still being representative in lower dimensions! These smaller datasets can then be fed into machine learning models to make predictions as usual, without worrying that reducing the size of the original dataset will hurt the accuracy of the predictions. So, we can now add to our formal definition of PCA to say that it is the process of finding a linear subspace with fewer dimensions in which the largest difference in the original dataset is kept.

Although these PCA components may make no sense for a human being, they make sense to the machine learning algorithms, as these algorithms only manage and deal with standardized numbers. 

<p align="center">
    <img src="https://user-images.githubusercontent.com/98360572/174354675-bcffff6b-5f7a-4930-9872-3464d9c448e3.png" width="50%" height="50%">
</p>

## Clustering Crytocurrencies Using K-Means
**K-means** clustering is one of the easiest and most popular algorithms for unsupervised machine learning.

Most of the time, unsupervised algorithms draw conclusions from datasets by only looking at input vectors and not at known, or labeled, outcomes.

The goal of **K-means** is simple: group similar data points together and find underlying patterns.  **K-means** looks for a fixed number (k) of clusters in a dataset to reach this goal.

A cluster is a group of data points that are put together because they have some things in common.

You will set a target number, k, which is the number of centers you need in the dataset. A centroid is the place, real or made up, that represents the cluster's center.

Each data point is put into one of the clusters by lowering the sum of squares for each cluster.

In other words, the **K-means** algorithm finds k number of centers, then puts each data point in the cluster that is closest to it while keeping the centers as small as possible.

The word "means" in **K-means** refers to taking the average of the data, or finding the center.

In the **Elbow method**, the number of clusters (K) can be anywhere from 1 to 10. The WCSS (Within-Cluster Sum of Square) is calculated for each value of K. WCSS is the total squared distance between each point in a cluster and the center point.

When we plot the WCSS with the K value, the graph looks like an Elbow. The WCSS value will start to go down as the number of clusters goes up. When K = 1, the WCSS value is the highest. When we look at the graph, we can see that at one point, it changes quickly, making an elbow shape. From here, the graph starts to move in a direction that is almost parallel to the X-axis. At this point, the K value that goes with it is the best K value or the best number of clusters.

<p align="center">
    <img src="https://user-images.githubusercontent.com/98360572/174356539-c9d8b597-6167-4c5b-8614-157ed35cf0e6.png" width="100%" height="100%">
</p>

<p align="center">
    <img src="https://user-images.githubusercontent.com/98360572/174355202-b82350d6-bde8-45f2-944e-3e4616e8e0f9.png" width="100%" height="100%">
</p>

## Visualizing Cryptocurrencies Results
A cluster in a scatter plot is a group of points that follow the same general pattern. They could follow a linear pattern or a curved pattern. Clusters can contain many points.

### 3D-Scatterplot with Clusters
<p align="center">
    <img src="https://user-images.githubusercontent.com/98360572/174356267-ced9fb23-180e-4aec-98c7-9f4411911ca4.png" width="100%" height="100%">
</p>

### Scatterplot
<p align="center">
    <img src="https://user-images.githubusercontent.com/98360572/174355872-f770fd59-0010-4c3d-9a65-4c2743c46039.png" width="100%" height="100%">
</p>

### Interactive Table
I used the hvplot library to make an interactive table. When the column header is clicked, the values in that column are put in order. This interactive table is a great way to find out what coins can be traded, what algorithms are used, and how they can be sorted in ascending or descending order.

<p align="center">
    <img src="https://user-images.githubusercontent.com/98360572/174357160-1c6f7888-a55c-47f9-af03-eabbc6451b1a.png" width="100%" height="100%">
</p>

---
# :three: References.

Using Unsupervised Learning to Discover Unknown Patterns, https://courses.bootcampspot.com/courses/1145/pages/18-dot-0-1-using-unsupervised-learning-to-discover-unknown-patterns

Copy Paste Guru: How to fix "ModuleNotFoundError: No module named 'hvplot'", https://copypaste.guru/WhereIsMyPythonModule/how-to-fix-modulenotfounderror-no-module-named-hvplot

Towards Data Science: Get Started: 3 Ways to Load CSV files into Colab, https://towardsdatascience.com/3-ways-to-load-csv-files-into-colab-7c14fcbdcb92

Holoviz, Hvplot: Plotting, https://hvplot.holoviz.org/user_guide/Plotting.html
 
Github: Colab rendering requires reloading extension in each cell #3551, https://github.com/holoviz/holoviews/issues/3551

Github: df.hvplot() not working in colab #153, https://github.com/holoviz/hvplot/issues/153
