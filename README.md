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
![img2](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/158031487/de1f9490-abe6-470c-8132-a7e94183fe75)

## After Performing K-Means and removing one cluster
![image](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/158031487/de3e3f86-1fb3-476c-929c-b43bade09da3)

## After Performing DBSCAN and removing a range of clusters
![image](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/158031487/8551210b-f646-4fa7-a0b9-e7e2e360769d)

## Using Canny edge detector and then find contours
![image](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/158031487/618fb2a9-245b-4884-84d6-59cc4e0590b0)

## Find bounding boxes formed after edge detection on images that have been clustered by DBSCAN
![image](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/158031487/135cbe46-9f12-4d38-b24c-f4b89a974d8f)

## Find bounding boxes formed after edge detection on images that have been clustered by K-Means
![image](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/158031487/43864231-72bc-44d1-bc97-8d153049b3a3)

## Appling Segment Anything Model
![image](https://github.com/codes-by-vamshi/CV-Mango-Orchards/assets/158031487/05d438ef-6e2d-446d-9c84-9720a9bdd16a)

## Taking Contour Centers and sending it to SAM


 ## References

  [0] https://github.com/sanjanprakash/Color-based-Image-Segmentation-using-K-Means-clustering
  
  [1] https://link.springer.com/chapter/10.1007/978-3-642-27311-7_79
  
  [2] https://www.modelbit.com/blog/deploying-a-segment-anything-image-recognition-model-to-a-rest-endpoint
