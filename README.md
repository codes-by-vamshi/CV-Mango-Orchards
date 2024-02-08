# CV-Mango-Orchards

## Introduction

Our main goal is to ensure the well-being of trees by optimizing sunlight penetration and promptly detecting areas where pruning is necessary. To achieve this, our primary step involves identifying all the unique trees within the provided images. This phase sets the foundation for subsequent analyses. By pinpointing individual trees, we can then proceed to assess their current health and identify areas where pruning may be necessary.

## Methods used to Identify trees

  1.Color based Clustering using K-Means to cluster trees from background.

  2.Color based Clustering using DBSCAN to cluster trees from background.

  3.Used Canny edge detector to then find the bounding boxes. 

  4.Used pre trained Segment Anything Model(SAM) by meta.

  5.We used the the centers of the bounding boxes from step 3 to segment the trees using SAM.
## Note: 
The Data Set is collection of drone images from a Mango Orchards from Uttar Pradesh, India. As the Data Set is from a Research Project and is not available for the public, we are providing a sample of 5 images only.

## The flow of the code with one example:

## Original Image 
![img1](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/71136812/2a80b68f-facd-46fe-89fc-fe13975c33a4)

## After Performing K-Means and removing one cluster
![image](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/71136812/b340c606-bede-4005-b516-8c22f747133f)

## After Performing DBSCAN and removing a range of clusters
![image](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/71136812/06dca782-c966-457a-a85b-c4f795cef56a)

## Using Canny edge detector and then find contours
![image](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/71136812/59bd465a-a21c-47eb-8e3c-d77c05d6a7a4)

## Find bounding boxes formed after edge detection on images that have been clustered by DBSCAN
![image](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/71136812/9b6a9ce1-faf4-4de2-b1a7-2e4eda9758de)

## Find bounding boxes formed after edge detection on images that have been clustered by K-Means
![image](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/71136812/b7f58016-f17b-48f4-86ad-71fb77ef8bd0)

## Appling Segment Anything Model
![image](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/158031487/05d438ef-6e2d-446d-9c84-9720a9bdd16a)

## Taking Contour Centers and sending it to SAM
![image](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/71136812/7a952dd1-8844-45d8-9fbb-e297f07af9a1)

 ## References

  [0] https://github.com/sanjanprakash/Color-based-Image-Segmentation-using-K-Means-clustering
  
  [1] https://link.springer.com/chapter/10.1007/978-3-642-27311-7_79
  
  [2] https://www.modelbit.com/blog/deploying-a-segment-anything-image-recognition-model-to-a-rest-endpoint
