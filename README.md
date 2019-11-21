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
 
  #### Original Image
 ![image](https://user-images.githubusercontent.com/46167070/69013175-ef669800-0985-11ea-8a6a-d08f8ae63e89.png)
 # Ground Truth :
 Ground truth: That is the reality you want your model to predict.

It may have some noise but you want your model to learn the underlying pattern in data that’s causing this ground truth. Practically, your model will never be able to predict the ground truth as ground truth will also have some noise and no model gives hundred percent accuracy but you want your model to be as close as possible.

 ![4](https://user-images.githubusercontent.com/46167070/69377529-2524bd00-0cb5-11ea-9c77-25cc2042f9a9.PNG)
![1](https://user-images.githubusercontent.com/46167070/69377531-25bd5380-0cb5-11ea-816d-9e289d575b49.PNG)
![2](https://user-images.githubusercontent.com/46167070/69377532-25bd5380-0cb5-11ea-9323-f93674274665.PNG)

 # K-Means clustering algorithm for RGB Images :
 K-Means clustering algorithm is an unsupervised algorithm and it is used to segment the interest area from the background. It clusters, or partitions the given data into K-clusters or parts based on the K-centroids.
The algorithm is used when you have unlabeled data(i.e. data without defined categories or groups). The goal is to find certain groups based on some kind of similarity in the data with the number of groups represented by K , chosen Values For K =[3,5,7,9,11]
##  For K = 3 
![image](https://user-images.githubusercontent.com/46167070/69378791-c6ad0e00-0cb7-11ea-9121-d30b9ae0d5bc.png)

 


  #### Kmeans Results :
 ![image](https://user-images.githubusercontent.com/46167070/69013329-85e78900-0987-11ea-8d87-ed297f3fc71b.png)

![image](https://user-images.githubusercontent.com/46167070/69013349-a31c5780-0987-11ea-9087-184f91646ed9.png)

![image](https://user-images.githubusercontent.com/46167070/69013390-ed9dd400-0987-11ea-8528-23c5314f47c2.png)
# F1 Score
is needed when you want to seek a balance between Precision and Recall. Right…so what is the difference between F1 Score and Accuracy then? We have previously seen that accuracy can be largely contributed by a large number of True Negatives which in most business circumstances, we do not focus on much whereas False Negative and False Positive usually has business costs (tangible & intangible) thus F1 Score might be a better measure to use if we need to seek a balance between Precision and Recall AND there is an uneven class distribution (large number of Actual Negatives).
![image](https://user-images.githubusercontent.com/46167070/69375033-05d76100-0cb0-11ea-9188-659045d8fe3f.png)

![image](https://user-images.githubusercontent.com/46167070/69377898-d88db180-0cb5-11ea-9939-4b4537c08623.png)

# Entropy :
We used shannon entropy to ignore the ZERO probability leads to Nan in results
There are essentially two cases and it is not clear from your sample which one applies here.
(1) Your probability distribution is discrete. Then you have to translate what appear to be relative frequencies to probabilities
(2) Your probability distribution is continuous. In that case the values in your input needn't sum to one. Assuming that the input is sampled regularly from the entire space, you'd get


# Big Image 
## A-Normalized Cut 
Affinity matrix: Affinity matrix is a  matrix with each element the affinity between data point $  In this project we use intensity-based affinity and distance-based affinity. The kernel size sigma of these two affinity is tricky. For intensity based affinity, the kernel  should be small, because two data points with large intensity difference should not be in same cluster by all means. for distance-based affinity, the kernel  should not be too small, because even two data points are far away, they can still be in same cluster, hence the restriction of distance affinity should be looser.
we Chose 5 Random Pictures Comparing their Kmeans Clustering and Normalized Cut



## Picture Number 47 

![11](https://user-images.githubusercontent.com/46167070/69379786-c9106780-0cb9-11ea-9063-d0d6c085e672.PNG)
![46a](https://user-images.githubusercontent.com/46167070/69379787-c9a8fe00-0cb9-11ea-8b03-6e8aa8ec6329.PNG)
## Picture Number 25
![25](https://user-images.githubusercontent.com/46167070/69379823-e0e7eb80-0cb9-11ea-8366-fbe78ac23f65.PNG)
![25a](https://user-images.githubusercontent.com/46167070/69380038-4c31bd80-0cba-11ea-9583-c504162cbc1b.PNG)

## Picture Number 7
![output-onlinepngtools](https://user-images.githubusercontent.com/46167070/69382034-d5e38a00-0cbe-11ea-9a08-ac26e16ab967.png)
![7](https://user-images.githubusercontent.com/46167070/69382035-d5e38a00-0cbe-11ea-9080-4f925708ab9e.PNG)


## Picture Number 14
![output-onlinepngtools (1)](https://user-images.githubusercontent.com/46167070/69381029-89974a80-0cbc-11ea-88de-43376a8e3bd3.png)
![14](https://user-images.githubusercontent.com/46167070/69381030-89974a80-0cbc-11ea-9070-de2efbe1b198.PNG)
## Picture Number 32
![a32](https://user-images.githubusercontent.com/46167070/69381091-a469bf00-0cbc-11ea-85eb-a24ec79c3cc6.PNG)
![32](https://user-images.githubusercontent.com/46167070/69381092-a5025580-0cbc-11ea-823b-b26ebbf90c6e.PNG)



