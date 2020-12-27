# Module 3 Project - Tanzanian Water Wells


## Introduction

Tanzania is a country located in East Africa in a region known as the Great Lakes Region. Currently, Tanzania is having a [water crisis](https://water.org/our-impact/where-we-work/tanzania/) in which 30 million people, out of a population of roughly 57 million people, lack access to a sanitary source of water. In this project, I will be using various machine learning models on data from [Driven Data's Pump It Up: Data Mining the Water Table Competition](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/page/23/)in order to determine the functionality of water wells in Tanzania. The purpose of this competition is to determine what wells are functional, functional, but need repairs, and non-functional in order to improve maintenance operations so that clean and useable water is available to the people of Tanzania.

Since the dataset from Driven Data is a multiclassification data set, I decided to work with three different machine learning models in order to determine which was best at producing the strongest model for this competition. I used k-Nearest Neighbor, Random Forest, and XGBoost in order to determine which machine model would produce the most viable performance. After running my models, I tested their accuracy by uploading my model results to the Driven Data competition. The following results were produced:

![Driven Data Model Scores](https://github.com/PNarducci1690/Proj_3_Tanzanian_Water_Wells/blob/main/images/Driven%20Data%20Model%20Scores.png)

For my purposes, I will only be discussing my data in terms of the Random Forest Classifier model that I created because it produced a score of .8081 when compared to my k-Nearest Neighbors and XGBoost Classifier models.

## Results

![RF Model Feature Importance](https://github.com/PNarducci1690/Proj_3_Tanzanian_Water_Wells/blob/main/images/Feature%20Importance.PNG)

In order to determine what features had the most significant impact on my RF model, I used the .feature_importances_ method in order to create a bar graph of the top 20 important features. According to the graph, Latitude and Longitude were the two major factors used when determining the best value for this model. 

![Well Functionality Location](https://github.com/PNarducci1690/Proj_3_Tanzanian_Water_Wells/blob/main/images/LatLong_wells.PNG)

The map may show where these wells may be located, but it does not explain why the wells are located in these areas. When looking at the next most important features, such as population, I noticed that most wells are situated near populated areas. 

![Well Functionality and Population Density](https://github.com/PNarducci1690/Proj_3_Tanzanian_Water_Wells/blob/main/images/pop_well.PNG)

Also, if a well is functional, it is found at a higher GPS height. 

![Well Functionality and GPS Height](https://github.com/PNarducci1690/Proj_3_Tanzanian_Water_Wells/blob/main/images/GPS_height.PNG)

These other factors helped to provide some reasoning as to why the wells would be located in certain areas where one might not expect wells to be. 

## Further Research

Even though my model did very well at determining well functionality when compared to the top value on Driven Data (.8294), there are many other methods that I would like to explore when returning to this dataset and producing an even stronger model:

* Using Catboost to mean encode my categorical features instead of one-hot-encoding them.
* Using SMOTE or cost-sensative learning to deal with multiclass imbalaces.
* Using permutation importance and/or Drop-Column importance in order to determine what features will help in producing a better model.
* Using pipelines in order to stream line my models.




