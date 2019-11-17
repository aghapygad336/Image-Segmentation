# Assignment(Image Segmentation): 
Image segmentation is the classification of an image into different groups. Many researches have been done in the area of image segmentation using clustering. There are different methods and one of the most popular methods is k-means clustering algorithm. K -means clustering algorithm is an unsupervised algorithm and it is used to segment the interest area from the background.

# Berkeley Segmentation Data Set and Benchmarks 500 (BSDS500):

Best Practice Guidelines: The dataset consists of 500 natural images, ground-truth human annotations and benchmarking code. The data is explicitly separated into disjoint train, validation and test subsets. In order to preserve the integrity of the evaluation and obtain a direct and fair comparison of your results with existing methods
![Exemplary-segmentation-results-on-Berkeley-BSDS-500-obtained-on-the-optimal-database](https://user-images.githubusercontent.com/46167070/69013051-7fa3dd80-0984-11ea-87ec-feff1e516b88.png)

## Train only on trainval:
All the learning, parameter tuning, model selection, etc. should be done exclusively on the train and validation subsets of the data.

## Run once on test:
After training, your algorithm should be run only once with fixed parameters on the test subset of the data. The images and ground-truth segmentations of the test set cannot be used for tuning your algorithm.

## the evaluation results: 
Evaluate your results on the test subset with the Kmeans code. In order to assess quantitatively different aspects of performance of contour detection and segmentation algorithms, the BSDS500 provides a suite of evaluation measures.
 
 # K-Means clustering algorithm :
 K-Means clustering algorithm is an unsupervised algorithm and it is used to segment the interest area from the background. It clusters, or partitions the given data into K-clusters or parts based on the K-centroids.
The algorithm is used when you have unlabeled data(i.e. data without defined categories or groups). The goal is to find certain groups based on some kind of similarity in the data with the number of groups represented by K , chosen Values For K =[3,5,7,9,11]
 
 
 #### Original Image
 ![image](https://user-images.githubusercontent.com/46167070/69013175-ef669800-0985-11ea-8a6a-d08f8ae63e89.png)
 
  #### Kmeans Results :
  

