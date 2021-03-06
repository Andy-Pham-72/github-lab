# GoodVitamins

![goodvitamins](https://user-images.githubusercontent.com/70767722/123291518-2dbc2580-d4e0-11eb-98dc-27bdf4e6d1d9.jpeg)


Applying NLP and unsupervised machine learning technique to quickly showing the top representative user reviews of vitamin products from iHerb

## Introduction
Supplements are regulated by the FDA. However, the framework is different from drugs. The FDA does not review dietary supplement products for safety and effectiveness before they are marketed which leads to a question: Are all the supplements effective?
The good answer is to look at the users' reviews, nevertheless, one popular product can have thousands of reviews which can be time-consuming for the buyer to read through all and there will be lots of repetitive contexts.

This is when GoodVitamins algorithm comes in handy, it can process thousands of reviews down to the top representative of reviews. The process consists of transforming each review contents into 512-dimentional vectors (using the [Universal Sentence Encoder](https://tfhub.dev/google/universal-sentence-encoder/4) from TensorFlow Hub) and locating the different cluter centers on the high-dimensional space (using [K-means Clustering](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html)) and extracting the review vector which is closest to the cluster center (using the simple inner product calculation).

To learn more, please check:
 * The walk-through video: [GoodVitamins - Demo presentation](https://www.loom.com/share/508d15512d2a49fc831e01c6387f3e40)

 * Web app: [GoodVitamins - An Interactive Vitamin Product Review Summarization App From iHerb](https://goodvitamins.herokuapp.com)
 
 * The [Notebooks](https://github.com/Andy-Pham-72/GoodVitamins/tree/main/notebooks)

## Notebooks
Detailed notebooks of how the algorithm was created and other exploratory analysis within the project.

* `01_Data_cleaning_text_preprocessing_exploration` : Data cleaning process, text preprocessing and EDA process.
* `02_Modelling_for_GoodVitamins`                  : Explains the concept of the project algorithm.
* `03_Optimizing_the_k-means_Clustering_model`     : Explains the how to optimize the optimal cluster number.
* `04_Exploring_DBSCAN_with_the_dataset`           : Experiments DBSCAN with the dataset.
* `05_Visualizing_results`                         : An attempt to visualize the result.

## Datasource
Dataset for GoodVitamins comes from the Bestselling Vitamin Product pages on iHerb. 

* `iHerb_best_seller_products_scraper`             : self-made python web scraping script using Selenium notebook.

## Note

GoodVitamins project was created as part of my capstone project for my Data Science Diploma at [BrainStation](https://brainstation.io).

The framework of GoodVitamins were inspired by the project [BetterReads](https://github.com/williecostello/BetterReads) by [Willie Costello](https://www.linkedin.com/in/williecostello/). It's such a big help for me to finish my capstone project.

I would like to thank my educators: [Adam Thorsteinson](https://www.linkedin.com/in/adam-thorsteinson-670a0552/), [Govind Suresh](https://www.linkedin.com/in/govindsuresh/), [Luan Nguyen](https://www.linkedin.com/in/lnguyen7-nd/), and [Ben Polzin](https://www.linkedin.com/in/bpolzin/). Last but not least, many thanks to my amazing classmates.
