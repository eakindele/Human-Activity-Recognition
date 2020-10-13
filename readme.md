## Introduction and Purpose  

Movement is an important part of maintaining a healthy lifestyle. For many, the advent of the coronavirus has made it all too simple to spend countless hours seated indoors in front of their computers while working, or in front of television sets for entertainment. As such, the ability to alert users of their activity levels is more important than ever. 


## Problem Statement

In this project, I sought out to build a Human Activity Recognition System that identifies a task as sitting, standing, walking, jogging, upstairs or downstairs based on data from an accelerometer worn on the wrist.

## Data Cleaning
[The data can be found here](https://archive.ics.uci.edu/ml/datasets/selfBACK)  

Not much needed to be done in the way of cleaning, as the dataset was well kept. Each participant's activities were stored in individual csv files, so I wrote some code to read all of them in. Additionally, because of how I needed to scale my data, I randomly selected participants to be in a training or testing set of the data. 


## Data Preprocessing:

An individual sample from an accelerometer does not give much insight into what is occurring. For example, a person sitting and talking, could resemble gestures used by a person standing and talking. This mimicry could be confusing to a computer in an individual sample, but becomes more clear when put into context with a few other samples. For this reason, I will look at overlapping segments of time, called windows, to allow the computer to learn.

Additionally, people of differing arm lengths are bound to have differences in accelerometer magnitude - for example, a longer person’s walk could be confused with a smaller person’s run. As such, I will also scale my data down to avoid such confusion.

## Modeling

The model I have included in my repo is my best performing model. I used a CNN which achieved about 85% accuracy. The reason I tried modeling with a CNN is because of how well they tend to perform in pattern recognition. Additionally, I wanted to add a piece to my repo to showcase my understanding of neural network models.


## Conclusion

I built a reasonable successful model, the area in which it struggles the most was confusing upstairs and downstairs activities. This could have been due to the fact that the dataset was imbalanced. Both stairs activities had about half as many samples as the other ones in the data set.

## Future Work

I would like to come up with a scoring metric that allows users to know how their activties vary day to day. I would also like to see the difference in model performance of wrist based accelerometers vs phones.

## Data Directory
|__ UCI_Data
| |__ w  
| |  |__ sitting  
| |  |__ standing  
| |  |__ walking  
| |  |__ jogging  
| |  |__ upstairs
| |  |__ downstairs 
|__ EDA.ipynb  
|__ Preprocessing_and_Modeling.ipynb  
|__ Human Activity Recognition with Wrist-Based Accelerometers.pdf