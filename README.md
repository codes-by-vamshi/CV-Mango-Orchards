# CV-Mango-Orchards

## Introduction

Our main goal is to ensure the well-being of trees by optimizing sunlight penetration and promptly detecting areas where pruning is necessary. To achieve this, our primary step involves identifying all the unique trees within the provided images. This phase sets the foundation for subsequent analyses. By pinpointing individual trees, we can then proceed to assess their current health and identify areas where pruning may be necessary.

## Methods used to Identify trees

  1.Color based Clustering using K-Means to cluster trees from background.

  2.Color based Clustering using DBSCAN to cluster trees from background.

  3.Used Canny edge detector to then find the bounding boxes. 

  4.Used pre trained Segment Anything Model(SAM) by meta.

  5.We used the the centers of the bounding boxes from step 3 to segment the trees using SAM.

## References

  [0] https://github.com/sanjanprakash/Color-based-Image-Segmentation-using-K-Means-clustering
  
  [1] https://link.springer.com/chapter/10.1007/978-3-642-27311-7_79
  
  [2] https://www.modelbit.com/blog/deploying-a-segment-anything-image-recognition-model-to-a-rest-endpoint
