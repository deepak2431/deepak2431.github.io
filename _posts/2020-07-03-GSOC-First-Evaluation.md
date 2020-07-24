---
layout: post
title: GSoC'20 First Evaluation
category: Tech
---


Hello everyone,

In the last blog, I wrote about my first two weeks on the GSoC period. In this blog, I will write about the activities on which I have worked further to implement multiple datasets.

Until now, I have implemented the multiple datasets in the following activities:

1. Enumeration memory game
2. Addition memory game with Tux and without Tux
3. Subtraction memory game with Tux and without Tux
4. Multiplication memory game with Tux and without Tux

### Why multiple datasets for GCompris activities?

 All of the GCompris activities had a generalized dataset. For some of the age groups like 3-5 yrs the activity were quite difficult to play, while for older age groups the activity were easy. So, multiple datasets helps in resolving this issue and making the activity adaptive for children of all age groups.

### Enumeration memory game

In this activity, the child needs to turn the cards to count the images and match with the corresponding number cards. I started my work of implementing multiple datasets to memory activities with this activity. To do this I needed to change the logic of the code to support both the default datasets and the multiple datasets. I made the required changes to the code and added multiple datasets to enumeration memory game activity. After implementing multiple datasets there was an issue in case of just two pairs as the level doesn't gets loaded. To fix this issue I updated the condition which checks that the resources of images, sounds, texts are enough to load a particular level or not. There is a total of 8 multiple datasets for this activity. <br>
Below image shows the dataset screen for Enumeration memory game activity

![enumeration-multiple-datasets](https://user-images.githubusercontent.com/66898390/86505756-55edd880-bde6-11ea-86e4-88a3d73ff9aa.png)

After implementing multiple datasets for this activity there was a regression that affected all memory activities. The regression was that a blank activity config was displayed for activities with no multiple datasets. I fixed this regression too and pushed the changes to my branch for review. Once I had everything perfectly done and tested, I made a merge request from my working branch so that it could be merged to master. 

### Addition memory game

In this activity, the child needs to turn the cards to match an addition and its result, until all the cards are gone. The goal of this activity is to practice addition. After the implementation of multiple datasets for enumeration memory games it's not that difficult to add multiple datasets for other memory activities. We just need to create different Data.qml files in the resource directory and load the datasets. For this activity we need to use the function getAddTable() implemented in math_util.js and pass the arguments for the respective numbers. In this activity there is a total of 10 multiple datasets. This activity has two modes. The first mode is the one in which child needs to turn the cards and match with the equivalent addition result. The second mode is the one in which child need to play with Tux to match the equivalent cards, as this mode is called "with Tux". I have implemented multiple datasets for both of the modes. The dataset content of the activity Addition memory game with Tux is the same as without Tux. Once I have implemented the datasets for both modes, I made a merge request from my working branch.

Code of Data.qml file 

```
import GCompris 1.0
import "qrc:/gcompris/src/activities/memory/math_util.js" as Memory

Data {
    objective: qsTr("Addition table of 1.")
    difficulty: 4

    data: [
        { // Level 1
            columns: 5,
            rows: 2,
            texts: Memory.getAddTable(1)
        }
    ]
}
```

You can see that the content of the dataset is in json format. And to just add another multiple dataset we need to change the number from 1 to 2 and update the goal. Quite easy to add ten multiple datasets :)<br>
Below image shows the dataset screen for Addition memory game activity

![addition-memory-games](https://user-images.githubusercontent.com/66898390/86506233-25f50400-bdeb-11ea-8e8d-6988a4f397da.png)


### Subtraction memory game

In this activity, the child needs to turn the cards to match a subtraction and its result, until all the cards are gone. The goal of this activity is to practice subtraction. The datasets implementation procedure is same as for addition memory game just we need to use the getSubTable() function from math_util.js. This activity also have two modes as one with Tux and another without Tux. I have implemented multiple datasets to both modes of the activity.<br>
Below image shows the dataset screen for Subtraction memory game activity

![subtraction-memory-games](https://user-images.githubusercontent.com/66898390/86506339-2a6dec80-bdec-11ea-8885-7609f39b8f48.png)

### Multiplication memory game

In this activity, the child needs to turn the cards to match a multiplication and its result, until all the cards are gone. The goal of this activity to practice multiplication. The dataset implementation procedure is the same as for addition and subtraction memory game just we need to use the getMulTable() function from math_util.js. This activity also have two modes so I have implemented multiple datasets to both modes of the activity.<br>
Below image shows the datasets screen for Multiplication memory game activity

![multiplication-memory-games](https://user-images.githubusercontent.com/66898390/86506381-90f30a80-bdec-11ea-8447-65ef69975833.png)


### What's next?

I will further work on the implementation of multiple datasets to division memory game activity and other memory activities. As our project is moving to KDE Gitlab instance. I will push all of my further work there only on a different git branch for each activity group.

Regards<br>
Deepak Kumar



