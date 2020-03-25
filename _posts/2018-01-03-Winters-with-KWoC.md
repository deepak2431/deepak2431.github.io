---
layout: post
title: Winters with KWoC
category: Tech
---

This winter, I, along with a few other people, helped [@Aniq55] to work on this beauty of a game(!):


![](https://raw.githubusercontent.com/vineetjc/vineetjc.github.io/master/images/playscreen.png)

### Project Name: AirHockey
### Mentor: Aniq Ur Rahman ([@Aniq55])
[@Aniq55]: https://github.com/Aniq55

# About KWoC
KWoC (Kharagpur Winter Of Code) is an annual open-source program conducted by Kharagpur Open Source Society, IIT Kharagpur. It is a five-week long program that runs during the month of December. It is aimed at promoting open source participation and helping students prepare for events like GSoC.

# About AirHockey
AirHockey is the digital version of the Air Hockey game. This game is for two players and was made using Python 2.x and pygame. Read more [here]

[here]: https://github.com/NITDgpOS/AirHockey#about-air-hockey

# My Experience with Kharagpur Winter of Code

I'm very glad my elder sister told me about KWoC because there couldn't have possibly been a better way to spend my time last vacation. Kharagpur Winter of Code is an excellent initiative to get people started with contributing to projects and entering the world of Open Source. I had already worked with Git and GitHub before KWoC, but this was a new experience on its own. I worked with a team bigger than I thought it would be, thanks to the amazing turnout when students were choosing their projects. Since it was just one month of coding, I felt a greater need to submit whatever I'm working on as soon as possible. I learnt to open issues and become better with pull requests and messages on commits. Most importantly, I worked on a project I really liked and could commit to (pun intended). 

# My contributions:
### Overall: 6 commits, 94++ 82- - (As of January 5, 2018)
---
### Issue 1: Background music plays multiple times on round completion

#### Description: 
At the end of every round, the background music would play again over the already playing music, and this would repeat every round.
#### [Link to issue 1]
[Link to issue 1]: https://github.com/NITDgpOS/AirHockey/issues/97
#### [Commits to issue 1]
[Commits to issue 1]: https://github.com/NITDgpOS/AirHockey/pull/106

---

### Issue 2: Quit button on start screen not working 

#### Description: 
The red quit button at the bottom right of the start screen lead the user to the next screen instead of quitting the game.
#### [Link to issue 2] 
[Link to issue 2]: https://github.com/NITDgpOS/AirHockey/issues/145
#### [Commits to issue 2] 
[Commits to issue 2]: https://github.com/NITDgpOS/AirHockey/pull/148
Additional: Other than just fixing that button, I also added the functionality of the close button on the title bar of the game window. At any time, the user can now quit by just clicking the close button on the top right, just like any other application window.
#### Screenshot: 

![](https://raw.githubusercontent.com/vineetjc/vineetjc.github.io/master/images/quit.png)

---

### Issue 3: Errors in the end game screen

#### Description: 
Essentially an undefined variable (wrong variable name) in a function that ran at the completion of the game.
#### [Link to issue 3] 
[Link to issue 3]: https://github.com/NITDgpOS/AirHockey/issues/147
    
#### [Commits to issue 3] 
[Commits to issue 3]: https://github.com/NITDgpOS/AirHockey/pull/149

---

### Issue 4: Errors with colour selection highlighter on mouse click

#### Description:
The colour selection highlighter initially wouldn't update on mouse click but only with keys 'a' and 'd'.  On top of that, there was just one highlighter while it would have made more sense for both players to have a selection highlighter for themselves.
#### [Link to issue 4]
[Link to issue 4]:https://github.com/NITDgpOS/AirHockey/issues/162

#### Commits to issue 4:
[Updating with mouse click]

[Updating with mouse click]: https://github.com/NITDgpOS/AirHockey/pull/156

[Selector for both players]

[Selector for both players]: https://github.com/NITDgpOS/AirHockey/pull/167

###### Screenshot:

![](https://raw.githubusercontent.com/vineetjc/vineetjc.github.io/master/images/startscreen.png)

---

### Issue 5: Error with difficulty selection using keyboard 

#### Description:
Using 'e' and 'h', the user can select the difficulty of the game, 'Easy' or 'Hard', respectively. But with new updates, this function was not updated.
#### [Link to issue 5]
[Link to issue 5]: https://github.com/NITDgpOS/AirHockey/issues/187

### Issue 6: Issues with entering player names

#### Description: 
If only one player changed their name and if the other player box was left out, it wouldn't reflect correct changes in the game.
#### [Link to issue 6]
[Link to issue 6]: https://github.com/NITDgpOS/AirHockey/issues/186

### Issue 7: Wrong selected color displayed for Player 2

#### Screenshot:
![](https://raw.githubusercontent.com/vineetjc/vineetjc.github.io/master/images/error.png)

#### [Link to issue 7]
[Link to issue 7]: https://github.com/NITDgpOS/AirHockey/issues/188

#### [Commits to Issues 5, 6, 7] 
[Commits to Issues 5, 6, 7]: https://github.com/NITDgpOS/AirHockey/pull/189

---

# Future improvements in the Project

Some things that could be still incorporated into the project, or at least, those that I'd put forward as suggestions and later code it out and send a PR for, are

1. The game wasn't made to support fullscreen in the first place. However, I feel that it could be a nice feature to implement. It would require a lot of work and changes in the code, but it would be alright an add-on feature. 

2. One more thing that the contributors of the project could work on is to make it Python 2/3 agnostic. Currently, the game runs on Python 2.x, but that limits Python 3 users initially, till they get a 2.x version.

3. There are still some issues to cover that are pertinent - bot vs human match, making the game internet multiplayer etc. That would essentially make the game, in a way, complete.
    
It was a splendid experience working on this project over the winters, and I'm looking forward to contributing more to this project even after KWoC is now officially over for this year.

@Aniq55 has been a great mentor. 

KWoC was amazing and I can't wait for next year!
