---
layout: single
title:  "Decoding Meaning from Data: Utilizing Autoencoders for enhanced Pattern Recognition"
date: 2024-06-12
tags: "Machine Learning Autoencoder Neural Network Clustering"
header:
    overlay_image: "assets/image/ML3 BG.png"
---
Machine Learning \| Autoencoder \| Neural Network \| Clustering


This study explores the use of autoencoders as a data preprocessing step to improve feature separation by latent factor extraction. Data Compression through various methods is useful in Data Science to improve feature separation or as feature engineering or vectorization. Our study furthers this by attempting to make a universalizable method for preprocessing by using a proximity matrix and then an autoencoder to use relationships between rows as the primary features that we extract and use for clustering. Clustering is done with K-means and Ward’s clustering algorithms, and the best performing results are noted. We evaluate this method over five University of Irving public datasets commonly used as benchmarks and show in which cases that the method can effectively improve feature extraction and thus the clustering results.

The data used for this study can be found [here](https://scikit-learn.org/stable/datasets/toy_dataset.html)

**The study follows this general pipeline**
![Pipeline](assets/image/pipeline.jpg)


Final Results

**K-Means**
![K-Means](assets/image/K-means.jpg)

**Ward's Method**
![Ward's](assets/image/wards.jpg)

Insights:
1. Different Autoencoder architecture or preprocessing steps can extract different features to improve the performance of clustering
2. Domain Expertise can be applied to customize the preparation step
3. This can be applied into customer segmentation, anomaly detection, and product categorization


