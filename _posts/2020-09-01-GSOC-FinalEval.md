---
layout: post
title: Google Summer of Code Final Evaluation
category: Tech
---

Hi everyone,

In the previous blog I wrote about one of the major milestones I achieved. If you haven’t read it yet you can read it over here [Blog](https://deepak2431.github.io/GSOC9W/)

Google summer of code is going to end soon so in this project I would like to update about my work I have done this month. During this month I worked on two more activities after adding multiple datasets to memory activities. The two activities were:
1. Mirror the given image
2. Guess Count

### Mirror the given image 
In this activity, the child needs to draw the mirror of the given grid image using different colors. 
Before I was about to start my implementation of multiple datasets I found a bug, the mouse area for the last row grid was not working. I was not able to fill the colors of the last row grid in order to complete any levels. I reported it to my mentors to confirm about it once. Before I had time to fix this bug, one of my mentors did it. The multiple datasets were already present in this activity. My task was to improve multiple datasets as the initial grid size was not corresponding to the datasets difficulty levels. My mentors also asked me to add some details to the settings descriptions.

![Peek 2020-08-26 19-56](https://user-images.githubusercontent.com/44617923/91797174-911e5380-ec3f-11ea-9ff4-e984ce86cecb.gif)

This activity is now merged in the master.


### Guess count activity
In this activity, the child needs to drag the given operands to calculate the arithmetic result provided. This activity had two different modes, one as the "Builtin" and the other one as the "Admin" mode. There were no multiple datasets in this activity. After discussion with the mentors we agreed to separate the modes:

1. When selecting the Admin mode, the selection of the dataset must have no effect on the activity, as the activity must follow the levels/content specified in the Admin mode options.
2. When selecting the BuiltIn mode, the activity must use the content of the datasets for the multiple datasets.

To start with I separated both modes in such a way that loading one of the modes should not affect the other. I added the multiple datasets to it as I  implemented an algorithm so that the multiple datasets mode should use the same function used to build the admin mode datasets. I did this as I thought it won't be good to rewrite the same function twice with slight changes. After the review of the datasets by the mentors there was some improvement suggested for multiple dataset 4. As for it, there was only 1 level. I added two more levels to it. Also, it was mentioned in the multiple datasets parent task description that when selecting one of the modes it should disable the other mode. For this, I needed to make changes to the core DialogChooseLevel.qml file. I used a boolean to disable one mode in case another mode is active. 

After testing the builtin mode it was all good but there were some issues with the admin mode. I have fixed all of them before the deadline of GSoC work period.

![Peek 2020-08-28 22-23](https://user-images.githubusercontent.com/44617923/91797222-a85d4100-ec3f-11ea-823c-9a524c8ee857.gif)

I hope it will get merged to the master branch soon :)


Stay tuned for the Google Summer of Code Final Report.

Thanks!
Deepak Kumar







