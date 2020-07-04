---
layout: post
title: GSoC'20 First Evaluation
category: Tech
---


Hello everyone,

In the last blog, I wrote about my first two weeks on the GSoC period. In this blog, I would write about the activities to which I have worked further and implemented multiple datasets.

As till now, I have implemented the multiple datasets to the following activities:

1. Enumeration memory games
2. Addition memory games with Tux and without Tux
3. Subtraction memory games with Tux and without Tux
4. Multiplication memory games with Tux and without Tux

Why multiple datasets to GCompris activities?

As previously all of the activities were having a generalized dataset so for some of the age groups as for 3-5 yrs the activity seems quite difficult to play, and also for some of the age groups the activity seems to be quite easy. So, multiple datasets help in resolving this issue and we have multiple data for various age groups and all the activities can be more adaptive for the children.

### Enumeration memory games

In this activity, the child needs to turn the cards to count the images and match with the corresponding number cards. I started my work of implementing multiple datasets to memory activities with this activity. To implement multiple datasets to memory activities I need to change the logic of the code to support the default datasets and the multiple datasets too. After implementing multiple datasets there was some issue in case of just two images so I updated the condition too which checks that the resources as images, sounds, texts are enough to load a particular level or not. There are in total of 8 multiple datasets for this activity.


![enumeration-multiple-datasets](https://user-images.githubusercontent.com/66898390/86505756-55edd880-bde6-11ea-86e4-88a3d73ff9aa.png)

After implementing multiple datasets to this activity there was a regression that affected all memory activities as a blank activity config was displayed for activities with no multiple datasets. I fixed this too and pushed the changes to my branch for review. Once I have done everything perfectly and tested it I made a merge request from my working branch so that it can be merged to master. 

### Addition memory games

In this activity, the child needs to turn the cards over to find two numbers which add up the same, until all the cards are gone. The goal of this activity to practice addition. As after implementation of multiple datasets to enumeration memory games it's not that difficult to implement multiple datasets to other memory activities as just we need to create different Data.qml file in resource directory and load the dataset. For this activity we need to use the function getAddTable() implemented in math_util.js and pass the arguments for the respective numbers. In this activity there are total of 10 multiple datasets. This activity has two mode as other Addition memory games with Tux activity so I have implemented multiple datasets to this too. Once I have implemented the datasets to both mode of addition memory games, I made a merge request from my working branch.

Code of Data.qml file 

https://gist.github.com/deepak2431/f98f33cc3c65e1693a64e2d3e4d6d254

As it can been seen that the content of the dataset is in json format. And to just implement anoother multiple dataset we need to change the number from 1 to 2 and update the goal. Quite easy to implement all the ten multiple datasets :)


![addition-memory-games](https://user-images.githubusercontent.com/66898390/86506233-25f50400-bdeb-11ea-8e8d-6988a4f397da.png)


### Subtraction memory games

In this activity, the child needs to turn the cards over to find two numbers which subtract up the same, until all the cards are gone. The goal of this activity to practice subtraction. The dataset implementation procedure is same as that of addition memory games just we need to use the getSubTable() function from math_util.js. This activity also have two modes so I have implemented multiple datasets to both mode.

![subtraction-memory-games](https://user-images.githubusercontent.com/66898390/86506339-2a6dec80-bdec-11ea-8885-7609f39b8f48.png)

### Multiplication memory games

In this activity, the child needs to turn the cards over to find two numbers which multiply up the same, until all the cards are gone. The goal of this activity to practice multiplication. The dataset implementation procedure is same as that of addition and subtraction memory games just we need to use the getMulTable() function from math_util.js. This activity also have two modes so I have implemented multiple datasets to both mode.

![multiplication-memory-games](https://user-images.githubusercontent.com/66898390/86506381-90f30a80-bdec-11ea-8447-65ef69975833.png)


### What's next?

As I mentioned I have during the first evaluation coding period I have implemented multiple datasets to the above-mentioned activities. I tested them manually and also got it tested by my younger sister :). After review of all my merge requests from mentors they all were good and have been merged to master branch. 

I will further work on the implementation of multiple datasets to division memory games activity and other memory activities. As our project is moving to Gitlab now by the KDE administrator so I will be pushing all of my further works there only on the respective branch of the activity.



