# Change Detection for Deforestation from Satellite Images
This project was made as part of the Webnova Hackathon and aims to utilize satellite images to detect deforestation.
Global stats indicate that there has been large occurrence of deforestation 

source:https://www.globalforestwatch.org/dashboards/global/ 

Access to satellite images can help a lot to the cause of deforestation.

This project uses a change detection algorithm to identify changes in vegetation or land cover between two satellite images. The algorithm uses Principal Component Analysis (PCA) and K-Means clustering to detect changes.

# Code explanation 
The code can be broken down into several parts:

## find_vector_set:
This function takes the difference image and its size as input, and returns the vector set and mean vector.

## find_FVS:
This function finds the Feature Vector Space (FVS) for the difference image.

## clustering: 
This function applies K-Means clustering to the FVS.

## find_PCAKmeans: 
This is the main function that reads the input images, resizes them, calculates the difference image, and applies the change detection algorithm.


# Output
The output of the code is an image showing the detected changes between the two input images. The color scheme in the output image represents different clusters identified by the K-Means algorithm, each corresponding to a different kind of change detected between the two input images.

Please note that the colors themselves do not have a fixed meaning and can change across different runs of the code. Instead, the meaning of each color is determined by the clustering results of the K-Means algorithm in each run. You can use the average pixel value of each cluster (printed out by the code) to interpret what kind of changes each color represents.

For example, a color representing a cluster with a low average pixel value likely corresponds to areas of the image where there was little to no change detected. Conversely, a color representing a cluster with a high average pixel value likely corresponds to areas where significant changes were detected.

This work uses and enhances the work of opswami189
