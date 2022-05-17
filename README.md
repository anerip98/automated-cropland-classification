# Accurate Cropland Delineation from Multi-Temporal Satellite Images using Spatio-Temporal Edge Detection

This work was done as part of a research training/internship at the Space Application Center at the Indian Space Research Organization (ISRO)

In this study, a dual class cropland classification for the area of study is produced using pixel based machine
learning methods on Sentinel-2 satellite multi-spectral temporal images using the red, green, blue, near infrared and shortwave
infrared bands and derived indices - Normalized Difference Vegetation Index (NDVI), Normalized Difference Water Index
(NDWI) and Norm. The classification output of the various algorithms implemented is validated using ground truth values
provided by the Ministry of Forest and Agriculture of Slovenia. Finally, the accuracy of 3 gradient boosting machine
learning models - LightGBM, Catboost, and Random Forests for this classification problem are compared in order to
conclude that the Catboost algorithm with it’s default parameters is optimum for the problem of cropland delineation, resulting in
a classification accuracy of 91.2%.

## Data

The multi-spectral time series data used is free and open access data obtained using the eo-learn package in python
that downloads data from the European Space Agency’s (ESA) website. Sentinel-2 satellite images corresponding to the
study area were utilized for this. The area of interest for this study is a square box bounded region in Slovenia. 
Projected longitude and latitude values of the upper left and bottom right corners of this bounding
box into meters are ([357,737.03, 632593.82], [5016135.99, 5204957.80]).

<img src="https://github.com/anerip98/automated-cropland-classification/blob/main/images/roi.png" width=600>

## Ground Truth Data:

### 11-class:

<img src="https://github.com/anerip98/automated-cropland-classification/blob/main/images/slovenia.png" width=600>

### 2-class:

<img src="https://github.com/anerip98/automated-cropland-classification/blob/main/images/2_class_roi.png" width=600>

## Results

Accuracy of all models

<img src="https://github.com/anerip98/automated-cropland-classification/blob/main/images/accuracy.png" width=600>

Accuracy with Catboost (Best performing classifier)

<img src="https://github.com/anerip98/automated-cropland-classification/blob/main/images/catboost_conf.png" width=600>
