#**Yelp Restaurant Photo Classification (Kaggle Competition)**

##1. Problem
In this capstone project I aim to build a classification model that assigns multiple labels to photos of restaurants. The capstone project is based on a Kaggle Competition provided by Yelp company. 
Currently, restaurant labels are manually selected by Yelp users when they submit a review. Selecting the labels is optional, leaving some restaurants un- or only partially-categorized. But Yelp’s users upload an enormous amount of photos every day alongside their written reviews. This data set of restaurants photos can be turned into multiple tags using an automatic classification model. 

##2. Client
Yelp is an American multinational corporation headquartered in San Francisco, California. It develops, hosts and markets Yelp.com and the Yelp mobile app, which publish crowd-sourced reviews about local businesses.

##3. Data
The data set for the project is Yelp users’ uploaded images (.jpg file format) of restaurants and corresponding labels (or business ids). The Data Files can be downloaded from site: (https://www.kaggle.com/c/yelp-restaurant-photo-classification/data).

### List of the Data files:
 - *train_photos.tgz* - photos of the training set (469684 images; 6.64 GB)
 - *test_photos.tgz* - photos of the test set (474304 images; 6.71 GB)
 - *train_photo_to_biz_ids.csv* - maps the photo id to business id
 - *test_photo_to_biz_ids.csv* - maps the photo id to business id
 - *train.csv* - main training dataset. Includes the business id's, and their corresponding labels. 

###There are 9 business IDs (labels) that can be assigned to pictures:

Business ID # | Description
------------ | -------------
0| good_for_lunch
1| good_for_dinner
2| takes_reservations
3| outdoor_seating
4| restaurant_is_expensive
5| has_alcohol
6| has_table_service
7| ambience_is_classy
8| good_for_kids

##4. Aprroach
1. **Remove duplicated images** from the data sets (in case users uploaded the same picture multiple times by mistake or chain restaurants upload the same pictures on the website). 
2. **Image preprocessing** procedure will involve the following steps:
 - Computing a mean image across the training images and subtracting it from every image
 - Scale each image so that its values range from [-1, 1]
3. Implement **Linear classifer** using a subset of data (O(10000) images) (*Capstone project Milestone report?*). The implementation will consist of the following steps:
 - Randomly choose set of weights **W** and biases **b** 
 - Compute the loss functions using two methdologies:
   * **Multiclass Support Vector Machine (SVM)** (with hingle loss function, maybe try squared hingle loss). The loss function will be extended with the Regularization penalty (L2 norm). 
   * **Softmax** (cross enropy loss) with Regularization penalty. 
 - Optimization with Mini-batch gradient descent


##5. Deliverables

- Slide desk showing the problem statement, implemented approach and results
- IPython notebook with codes/codebook
- Intended score in the Kaggle completion is 0.7 (Mean F1-Score)

