 <p align="center">
 <img src="https://user-images.githubusercontent.com/98360572/174341767-797fc8f8-4899-482e-a72a-c0ad6b9e335c.png" width="100%" height="50%">
</p>

# Module 18 Challenge: Using Unsupervised Learning to Discover Unknown Patterns

Unsupervised learning, also known as unsupervised machine learning, uses machine learning algorithms to analyze and cluster unlabeled datasets. These algorithms discover hidden patterns or data groupings without the need for human intervention. Its ability to discover similarities and differences in information make it the ideal solution for exploratory data analysis, cross-selling strategies, customer segmentation, and image recognition.

---
# :one: Overview of the analysis.

* Prepocessing of the data: It is crucial that we preprocess our data before feeding it into our model, as the quality of the data and the relevant information that can be gleaned from it directly influences the model's capacity to learn.  During the preprocessing we need to deal with:
    - Null values
    - Missing values
    - Standardization: transform the values such that the mean of the values is 0 and the standard deviation is 1.
    - Handling Categorical Variables:  Categorical variables are variables that are discrete rather than continuous in nature. For example, an item's color is a discrete variable, while its price is a continuous variable.
* Use of PCA (Principal Component Analysis) to reduce the number of dimensions in the analysis.  Principal Component Analysis (PCA) is a well-known unsupervised learning technique for reducing data dimensionality. It improves interpretability while reducing information loss at the same time. It aids in the discovery of the most important features in a dataset and facilitates the charting of data in 2D and 3D. PCA aids in the discovery of a series of linear combinations of variables.
* Use Elbow Curve: One of the most important parts of any unsupervised algorithm is figuring out the best number of groups into which the data can be put. One of the most common ways to find this optimal value of k is the "Elbow Method."
* Use of K-means to cluster data points together: k-means is a method for grouping data that can be used for unseprvised machine learning. It can sort unlabeled data into a certain number of clusters based on how similar they are. 
* Visualizing the results with hvplot and Plotly graphic libraries.

---
# :two: Results.

The complete code of the Jupyter Notebook used for this project can be found here: [Jupyter Notebook Code]([https://github.com/Peteresis/Cryptocurrency/blob/5031775b54e064fb16f1cd32dbd73249a24b7640/crypto_clustering.ipynb])

|   ⚠️ **NOTE: Please click on any image to zoom**     |
| ----------- |

<p align="center">
    <img src="https://user-images.githubusercontent.com/98360572/173168123-b5938c25-d47f-4dd6-9c96-d84ccf90b493.png" width="75%" height="75%">
</p>


![image](https://user-images.githubusercontent.com/98360572/174353574-54fa1e69-9882-4710-82af-16ca2ece7994.png)


## Screenshots

|   ⚠️ **NOTE: Please click on any image to zoom**     |
| ----------- |

<p align="center">
    <img src="https://user-images.githubusercontent.com/98360572/173168123-b5938c25-d47f-4dd6-9c96-d84ccf90b493.png" width="75%" height="75%">
</p>

<p align="left">
<div class="row">
  <div class="column">
    <img src="https://user-images.githubusercontent.com/98360572/173164118-81231084-fd26-4ddf-85cf-c24ffd6267c0.png" width="40%" height="40%">
    <img src="https://user-images.githubusercontent.com/98360572/173163893-3ddda1c9-ed17-4687-a31a-7903f8e0b9b2.png" width="40%" height="40%">
  </div>
</div>
</p>


---
# :three: Summary.


---
# :four: References.

Using Unsupervised Learning to Discover Unknown Patterns, https://courses.bootcampspot.com/courses/1145/pages/18-dot-0-1-using-unsupervised-learning-to-discover-unknown-patterns

Copy Paste Guru: How to fix "ModuleNotFoundError: No module named 'hvplot'", https://copypaste.guru/WhereIsMyPythonModule/how-to-fix-modulenotfounderror-no-module-named-hvplot

Towards Data Science: Get Started: 3 Ways to Load CSV files into Colab, https://towardsdatascience.com/3-ways-to-load-csv-files-into-colab-7c14fcbdcb92

Holoviz, Hvplot: Plotting, https://hvplot.holoviz.org/user_guide/Plotting.html
 
Github: Colab rendering requires reloading extension in each cell #3551, https://github.com/holoviz/holoviews/issues/3551

Github: df.hvplot() not working in colab #153, https://github.com/holoviz/hvplot/issues/153
