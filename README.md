# Computer Vision Assignment Report

Title: Scene Recognition with Bag of Words

Student Name:杨钊

Student ID:11813227



### 1. Experimental Design

The scene recognition with bag of words algorithm is generally divided into four steps:

1. Extract the local feature vector of the image. In order to achieve a good classification effect,
   the extracted feature vectors need to have varying degrees of invariance, such as rotation,
   scaling, translation, etc. (SIFT or HOG)
2. Use the feature vector to extract representative vectors as words bag to form a visual dictionary
3. Perform visual word statistics on an image, and generally judge whether the similarity
   between a local area of the image and a word exceeds a certain threshold. In this way, the
   image can be expressed as a distribution of words, which completes the representation of
   the image.
4. Design and train a classifier to use the distribution of words in the image to classify images.

The process of the experiment:

1. Image feature representation: The image features are obtained by two independent methods. The first method is to directly obtain the tiny features of the image. The advantage of this method is it can finish the task with high speed, but the accuracy is relatively low. The final classification accuracy is almost about 20%. The second method is to construct a bag of-words model. The classification accuracy is about 60%. Compared with the tiny feature, it is greatly improved. The main problem is it costs much more time to calculate the features.
2.  Construct categorizer, the categorizers used in this project contain KNN categorizer and SVM categorizer.

### 2. Experimental Results Analysis
a)Using tiny image and KNN categorizer
![8YZ662~}OK }ZNYCV$5V5)D](https://user-images.githubusercontent.com/85725490/205179381-a90b08bf-c72a-4a45-bdb3-b7cb041e9180.png)

b)Using bag of words and KNN categorizer
![image](https://user-images.githubusercontent.com/85725490/205179439-d12ae3b3-82af-4985-bff4-53d3645f7d1a.png)

c)Using bag of words and SVM categorizer
![image](https://user-images.githubusercontent.com/85725490/205179479-efef01d9-246c-448f-85ce-8fa36beb5c12.png)




### 3. Bonus Report (If you have done any bonus problem, state them here)

