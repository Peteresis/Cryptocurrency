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
<p align="center">
    <img src="https://user-images.githubusercontent.com/98360572/174353574-54fa1e69-9882-4710-82af-16ca2ece7994.png" width="50%" height="50%">
</p>

## Dataframe with the three principal components
<p align="center">
    <img src="https://user-images.githubusercontent.com/98360572/174354675-bcffff6b-5f7a-4930-9872-3464d9c448e3.png" width="50%" height="50%">
</p>

## Clustering Crytocurrencies Using K-Means
<p align="center">
    <img src="https://user-images.githubusercontent.com/98360572/174356539-c9d8b597-6167-4c5b-8614-157ed35cf0e6.png" width="100%" height="100%">
</p>

<p align="center">
    <img src="https://user-images.githubusercontent.com/98360572/174355202-b82350d6-bde8-45f2-944e-3e4616e8e0f9.png" width="100%" height="100%">
</p>

## Visualizing Cryptocurrencies Results
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
