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
- Thivya Tamil Selvam
- Anbu Selvi A/P M Paramasivan
- Noah Brynner Wee Supitang
- Radwan Mohammed Rashed Mahdi

- [ ] **Objectives:**
- Break out the project goal into more specific objectives
- [insert]
- [insert]
- [insert]


##  B. ABSTRACT 

In late December 2019, a previous unidentified coronavirus, currently named as the 2019 novel coronavirus, emerged from Wuhan, China, and resulted in a formidable outbreak in many cities in China and expanded globally, including Thailand, Republic of Korea, Japan, United States, Philippines, Viet Nam, and our country (as of 2/6/2020 at least 25 countries). Covid-19 are Person-to-person transmission may occur through droplet or contact transmission and if there is a lack of stringent infection control or if no proper personal protective equipment available, it may jeopardize the first-line healthcare workers.

The best safety measure that can be taken is enforcing the people to wear a face mask whenever they are outside to slow down the COVID-19 infection rate. Mask wearing significantly reduced the amounts of various airborne viruses coming from infected patients, measured using the breath-capturing "Gesundheit II machine" developed by Dr. Don Milton, a professor of applied environmental health and a senior author of the study published April 3 in the journal Nature Medicine. In short, masks can help prevent the spread of COVID-19 and that the more people wearing masks, the better.

As for now, you as a Data Scientist or Machine Learning Engineer or Practitioner are going to use AI technology to recognize people whether they are wearing face mask or not in the public or open space.


![Coding]()
Figure 1 shows the AI output of detecting which user is not wearing a face mask or inappropriate face mask.


## C.  DATASET

We’ll review the dataset we use in our music recommendation system.

Million Songs Dataset contains of two files: triplet_file and metadata_file. The triplet_file contains user_id, song_id and listen time. The metadata_file contains song_id, title, release, year and artist_name. Million Songs Dataset is a mixture of song from various website with the rating that users gave after listening to the song.

There are 3 types of recommendation system: content-based, collaborative and popularity but we have only used content-based and popularity in our project.

## D   TRAINING RESULTS

After training the program, it now can recommend songs based on popularity and content. However, there is a great difference of succession between the two methods.

![image](https://user-images.githubusercontent.com/86180936/123402779-b0291000-d5da-11eb-8051-c83d73513220.png)

It is apparent that the method of recommending based on content have fluctuating results. It seems that the model is unable to correctly choose the right songs based on the content of a target song. Assumably, a subjective input such as the content of a song cannot be easily categorize by the model and thus the impercise output.

In contrary to content based recommendation, the model can easily recommend songs to the user based on popularity of the song.

![image](https://user-images.githubusercontent.com/86180936/123404891-e4510080-d5db-11eb-99d6-f68acd814962.png)

![image](https://user-images.githubusercontent.com/86180936/123404933-ee72ff00-d5db-11eb-9e8d-dd6a84d3b222.png)

As shown above, the model is able to consistently recommend any user the most popular song. This is thanks to popularity being a more objective input for the model to evaluate easily. 

From this comparison, more training will be required for recommending songs by content more than than by popularity.

## D.   PROJECT STRUCTURE

The following directory is our structure of our project:
## D.   PROJECT STRUCTURE

The following directories are our structure of our project:
- $ tree --dirsfirst --filelimit 5
- .
- ├── dataset
- │   ├── song_data.csv [1000001 entries]
- │   └── triplets_file.csv [1048576 entries]
- ├── music_recommender
- │   ├── popularityBased_recommender.py
- │   ├── contentBased_recommender.py
- │   └── Main.py
- └── trainMusicDatasetRecommendation.py

- 2 directories, 15 files


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



## E   TRAINING THE COVID-19 FACE MASK DETECTION

We are now ready to train our face mask detector using Keras, TensorFlow, and Deep Learning.

From there, open up a terminal, and execute the following command:

- $ python train_mask_detector.py --dataset dataset
- [INFO] loading images...
- [INFO] compiling model...
- [INFO] training head...
- Train for 34 steps, validate on 276 samples
- Epoch 1/20
- 34/34 [==============================] - 30s 885ms/step - loss: 0.6431 - accuracy: 0.6676 - val_loss: 0.3696 - val_accuracy: 0.8242
- Epoch 2/20
- 34/34 [==============================] - 29s 853ms/step - loss: 0.3507 - accuracy: 0.8567 - val_loss: 0.1964 - val_accuracy: 0.9375
- Epoch 3/20
- 34/34 [==============================] - 27s 800ms/step - loss: 0.2792 - accuracy: 0.8820 - val_loss: 0.1383 - val_accuracy: 0.9531
- Epoch 4/20
- 34/34 [==============================] - 28s 814ms/step - loss: 0.2196 - accuracy: 0.9148 - val_loss: 0.1306 - val_accuracy: 0.9492
- Epoch 5/20
- 34/34 [==============================] - 27s 792ms/step - loss: 0.2006 - accuracy: 0.9213 - val_loss: 0.0863 - val_accuracy: 0.9688
- ...
- Epoch 16/20
- 34/34 [==============================] - 27s 801ms/step - loss: 0.0767 - accuracy: 0.9766 - val_loss: 0.0291 - val_accuracy: 0.9922
- Epoch 17/20
- 34/34 [==============================] - 27s 795ms/step - loss: 0.1042 - accuracy: 0.9616 - val_loss: 0.0243 - val_accuracy: 1.0000
- Epoch 18/20
- 34/34 [==============================] - 27s 796ms/step - loss: 0.0804 - accuracy: 0.9672 - val_loss: 0.0244 - val_accuracy: 0.9961
- Epoch 19/20
- 34/34 [==============================] - 27s 793ms/step - loss: 0.0836 - accuracy: 0.9710 - val_loss: 0.0440 - val_accuracy: 0.9883
- Epoch 20/20
- 34/34 [==============================] - 28s 838ms/step - loss: 0.0717 - accuracy: 0.9710 - val_loss: 0.0270 - val_accuracy: 0.9922
- [INFO] evaluating network...

|      |    precision    | recall| f1-score | support |
|------|-----------------|-------|----------|---------|
|with_mask|0.99|1.00|0.99|138|
|without_mask|1.00|0.99|0.99|138|
|accuracy| | |0.99|276|
|macro avg|0.99|0.99|0.99|276|
|weighted avg|0.99|0.99|0.99|276|


![Figure 4](https://s3.amazonaws.com/stackabuse/media/creating-simple-recommender-system-python-pandas-2.png)

Figure 4: Figure 10: COVID-19 face mask detector training accuracy/loss curves demonstrate high accuracy and little signs of overfitting on the data

As you can see, we are obtaining ~99% accuracy on our test set.

Looking at Figure 4, we can see there are little signs of overfitting, with the validation loss lower than the training loss. 

Given these results, we are hopeful that our model will generalize well to images outside our training and testing set.


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

