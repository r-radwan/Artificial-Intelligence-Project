# Music Recommendation System

## A. PROJECT SUMMARY

**Project Title:** Music Recommendation System

Music recommender system is one in all the foremost used machine learning algorithms in recommendation systems. A recommender (or recommendation) system (or engine) could be a filtering system that aim to predict a rating or preference a user would offer to Associate in Nursing item, eg. a movie title, a product, a song, etc.

There are two main types of recommender systems we have used in our project: 

**1) Content-based recommender**
**2)Popularity based recommender**

**Content-based recommender**

This type of recommender system is user-specific classification downside. This classifier learns the user's likes and dislikes from the options of the song.

The most straightforward approach is **keyword matching**.

In a few words, the thought behind is to extract purposeful keywords gift in an exceedingly song description a user likes, rummage around for the keywords in different song descriptions to estimate similarities among them, and supported that, suggest those songs to the user.

How is that this performed?

In our project, since we have a tendency to operating with text and words, Term Frequency-Inverse Document Frequency (TF-IDF) is used for this matching method.

**Team Members:** 
- Thivya Tamil Selvam            (B031910442)
- Anbu Selvi A/P M Paramasivan   (BO31910062)
- Noah Brynner Wee Supitang      (B031910101)
- Radwan Mohammed Rashed Mahdi   (B031910453)

- [ ] **Objectives:**
- The objective is to provide music recommendation systems that fit listeners profile in terms of content-based and popularity-based  with continuation of past exploration.

##  B. ABSTRACT 

  According to Nielsen’s Music 360 2014 study, 93 % of the U.S. population listens to music, defrayal quite twenty five hours every week electronic jamming intent on their favorite tunes. Recommender systems have taken the diversion and e-commerce industries by storm. Amazon, Netflix, and Spotify square measure nice examples.

  In this project, we've designed, enforced and analyzed song recommendation systems exploitation varied algorithms. Music recommendation may be a terribly difficult drawback as we've to structure music during a method that we have a tendency to advocate the favourite songs to users that is rarely a precise prediction. it's dynamic and generally influenced by factors apart from users’ or songs’ listening history. We've used Million Song Dataset , a freely-available collection of audio options and data for 1,000,000 contemporary music genre tracks provided by Echo Nest, to seek out the correlations between users and songs and to find out from the previous listening history of users to provide recommendations for songs that users would like to pay attention most. We will discuss the issues we have a tendency to Janus-faced, ways we've enforced, results and analysis. We have achieved best results exploitation neural network cooperative filtering formula.

## C.  DATASET

We’ll review the dataset we use in our music recommendation system.

Million Songs Dataset contains of two files: triplet_file and metadata_file. The triplet_file contains user_id, song_id and listen time. The metadata_file contains song_id, title, release, year and artist_name. Million Songs Dataset is a mixture of song from various website with the rating that users gave after listening to the song.

There are 3 types of recommendation system: content-based, collaborative and popularity but we have only used content-based and popularity in our project.

I’ll then show you how to analyze our content based engine dataset using Keras and TensorFlow.









I’ll then show you how to implement a Python script to train a face mask detector on our dataset using Keras and TensorFlow.

We’ll use this Python script to train a face mask detector and review the results.

Given the trained COVID-19 face mask detector, we’ll proceed to implement two more additional Python scripts used to:

- Detect COVID-19 face masks in images
- Detect face masks in real-time video streams

We’ll wrap up the post by looking at the results of applying our face mask detector.


There is two-phase COVID-19 face mask detector as shown in Figure 2:

![Figure 2]()
Figure 2: Phases and individual steps for building a COVID-19 face mask detector with computer vision and deep learning 

In order to train a custom face mask detector, we need to break our project into two distinct phases, each with its own respective sub-steps (as shown by Figure 1 above):

- Training: Here we’ll focus on loading our face mask detection dataset from disk, training a model (using Keras/TensorFlow) on this dataset, and then serializing the face mask detector to disk

- Deployment: Once the face mask detector is trained, we can then move on to loading the mask detector, performing face detection, and then classifying each face as with_mask or without_mask

We’ll review each of these phases and associated subsets in detail in the remainder of this tutorial, but in the meantime, let’s take a look at the dataset we’ll be using to train our COVID-19 face mask detector.


Our COVID-19 face mask detection dataset as shown in Figure 3:

![Figure 3]()

Figure 3: A face mask detection dataset consists of “with mask” and “without mask” images. 

The dataset we’ll be using here today was created by PyImageSearch reader Prajna Bhandary.

This dataset consists of 1,376 images belonging to two classes:

- with_mask: 690 images
- without_mask: 686 images

Our goal is to train a custom deep learning model to detect whether a person is or is not wearing a mask.

How was our face mask dataset created?
Prajna, like me, has been feeling down and depressed about the state of the world — thousands of people are dying each day, and for many of us, there is very little (if anything) we can do.

To help keep her spirits up, Prajna decided to distract herself by applying computer vision and deep learning to solve a real-world problem:

- Best case scenario — she could use her project to help others
- Worst case scenario — it gave her a much needed mental escape

## D.   PROJECT STRUCTURE

The following directories are our structure of our project:
- $ tree --dirsfirst --filelimit 6
- .
- ├── dataset
- │   ├── song_data.csv [1000001 entries]
- │   └── triplets_file.csv [1048576 entries]
- ├── music_recommender
- │   ├── popularityBased_recommender.py
- │   ├── contentBased_recommender.py
- │   └── Main.py
- └── trainMusicDatasetRecommendation.py

- 3 directories, 6 files


The dataset/ directory contains the data described in the “Our recommendation system dataset” section.

There are two datasets song_data.csv and triplets_file.csv. song_data.csv dataset consist of 1000001 rows and 5 columns
which are song_id, title, release, artist name and year. While the triplets_file.csv dataset contains 1048576 rows and 3 columns
which are user_id, song_id and listen_count. The ong_data.csv dataset is holding the main data for the system and
the triplets_file.csv dataset contains the data that have been collected from the user and counting the time for each song being played.
According to the counter the recommender can predict the recommendation

Explanation of the three Python scripts:

- popularityBased_recommender.py: Accepts our input dataset and make the ‎recommendation for the user based on the data column 
counter that the source code will identify.

- contentBased_recommender.py: Processes the data based on the content. This will ‎process the song_data.csv dataset.

- Main.py: Manipulation of the objects and controlling of the system classes.

In the next sections, we will train our music recommender.



## E TRAINING RESULT

After training the program, it now can recommend songs based on popularity and content. However, there is a great difference of succession between the two methods.

![image](https://user-images.githubusercontent.com/86180936/123402779-b0291000-d5da-11eb-8051-c83d73513220.png)

It is apparent that the method of recommending based on content have fluctuating results. It seems that the model is unable to correctly choose the right songs based on the content of a target song. Assumably, a subjective input such as the content of a song cannot be easily categorize by the model and thus the impercise output.

In contrary to content based recommendation, the model can easily recommend songs to the user based on popularity of the song.

![image](https://user-images.githubusercontent.com/86180936/123404891-e4510080-d5db-11eb-99d6-f68acd814962.png)

![image](https://user-images.githubusercontent.com/86180936/123404933-ee72ff00-d5db-11eb-9e8d-dd6a84d3b222.png)

As shown above, the model is able to consistently recommend any user the most popular song. This is thanks to popularity being a more objective input for the model to evaluate easily. 

From this comparison, more training will be required for recommending songs by content more than than by popularity.

## F.  RESULT AND CONCLUSION

Detecting COVID-19 face masks with OpenCV in real-time

You can then launch the mask detector in real-time video streams using the following command:
- $ python detect_mask_video.py
- [INFO] loading face detector model...
- INFO] loading face mask detector model...
- [INFO] starting video stream...

[![Figure5](https://i9.ytimg.com/vi/jIUN4k0gE-Q/mq1.jpg?sqp=CKCh54MG&rs=AOn4CLBi6Ge6x7CWNenhJ7pK-LKRnwJvMA)](https://youtu.be/jIUN4k0gE-Q)

Figure 5: Mask detector in real-time video streams

In Figure 5, you can see that our face mask detector is capable of running in real-time (and is correct in its predictions as well.



## G.   PROJECT PRESENTATION 

In this project, you learned how to create a COVID-19 face mask detector using OpenCV, Keras/TensorFlow, and Deep Learning.

To create our face mask detector, we trained a two-class model of people wearing masks and people not wearing masks.

We fine-tuned MobileNetV2 on our mask/no mask dataset and obtained a classifier that is ~99% accurate.

We then took this face mask classifier and applied it to both images and real-time video streams by:

- Detecting faces in images/video
- Extracting each individual face
- Applying our face mask classifier

Our face mask detector is accurate, and since we used the MobileNetV2 architecture, it’s also computationally efficient, making it easier to deploy the model to embedded systems (Raspberry Pi, Google Coral, Jetosn, Nano, etc.).

[![demo](https://i9.ytimg.com/vi/pA9An19rEVQ/mq3.jpg?sqp=CKCh54MG&rs=AOn4CLAHhKrP9UG9l5h2Y2gJpaV4DDSZUw)](https://youtu.be/pA9An19rEVQ)

