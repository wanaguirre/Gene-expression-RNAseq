This repository is just to show and teach some Unsupervised ML methods used to solve Clustering problems throught Dimensionality Reduction.

# Gene-expression-RNAseq

In this repository I compare the effect of different dimensionality reduction methods on the final visualization, and also the clustering tecquine we could use after the dimensionality reduction.

Techniques applied:
- Dimensionality Reduction for Visualisation
  - t-SNE
  - Uniform Manifold Approximation and Projection (UMAP)
- Dimensionality Reduction for Clustering
  - Principal component analysis (PCA)
- K-means algorithm for Clustering (with Elbow and Silhouette methods)
- Sankey Diagram UMAP

---

### Background:

Starting from the data provided by the University California Santa Cruz [here](https://xenabrowser.net/datapages/?dataset=tcga_RSEM_gene_tpm&host=https%3A%2F%2Ftoil.xenahubs.net&removeHub=https%3A%2F%2Fxena.treehouse.gi.ucsc.edu%3A443), we want to know how the different Gene Expressions would be clustered.


### Task:

Use various techniques that can be used to reduce the dimensionality, to then be able to cluster the Gene Expressions. Also, other important part of this notebook is focus on the visualization of this high-dimensional datasets using Dimensionality Reduction techniques.

---
### Methodology

  - **Data Understanding:** 
    - It's difficult to handle this because we have 14460 features
    - Check if the df has NaN values and rows with missing values
    - Data visualization: Plot distribution of sample columns
    - Data visualization: Correlation Heatmap, Histograms and Box plots to check all the features (Distributions and Outliers)
 
  - **Dimensionality Reduction for Visualisation:**
    
**t-SNE**

<p align="center">
<image src="Notebooks/images/tSNE.jpg" width=500px/>
</p>


**UMAP**

<p align="center">
<image src="Notebooks/images/UMAP.jpg" width=500px/>
</p>

  - **Dimensionality Reduction for Clustering:**
    - Create a Pipeline where firstly we are going to scale the values and then apply the PCA
    - K-Means after PCA: select the ‘optimal’ number of clusters with the Elbow Method (for a 95% of variance)
      - Scale, PCA, K-Means
    - Create a Pipeline where firstly we are going to scale the values and then apply the UMAP
    - K-Means after UMAP
      - Scale, UMAP, K-Means
    - Compare both tecniques with given labels

**PCA visualization**

<p align="center">
<image src="Notebooks/images/PCA.png" width=700px/>
</p>

**Visualize cluster by t-SNE (PCA)**

<p align="center">
<image src="Notebooks/images/clustering_PCA.jpg" width=700px/>
</p>

**Visualize cluster by t-SNE (UMAP)**

<p align="center">
<image src="Notebooks/images/clustering_UMAP.jpg" width=700px/>
</p>

**Visualize comparation PCA - UMAP**

<p align="center">
<image src="Notebooks/images/comparation.jpg" width=700px/>
</p>

  - **Results:**
    - Sankey Diagram Kmean
   
**Sankey Diagram Kmean**

<p align="center">
<image src="Notebooks/images/sankey_kmean.png"/>
</p>

**Sankey Diagram UMAP**

<p align="center">
<image src="Notebooks/images/sankey_umap.png"/>
</p>
   
