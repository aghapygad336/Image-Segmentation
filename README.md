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




