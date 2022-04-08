# Pre-work - Amelie and Julian's Hide and Seek Memory Game

Amelie and Julian's Hide and Seek is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: Casey Anderson

Time spent: 16 hours spent in total

Link to project: https://glitch.com/~scented-lapis-hell

## Required Functionality

The following **required** functionality is complete:

* [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [x] "Start" button toggles between "Start" and "Stop" when clicked. 
* [x] Game buttons each light up and play a sound when clicked. 
* [x] Computer plays back sequence of clues including sound and visual cue for each button
* [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [x] User wins the game after guessing a complete pattern
* [x] User loses the game after an incorrect guess** (see optional features - 2 incorrect guesses allowed)

The following **optional** features are implemented:

* [x] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [x] Buttons use a pitch (frequency) other than the ones in the tutorial
* [x] More than 4 functional game buttons
* [x] Playback speeds up on each turn
* [x] Computer picks a different pattern each time the game is played
* [x] Player only loses after 3 mistakes (instead of on the first mistake)
* [x] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

* [x] Game features difficulty selection
* [x] Users must choose between three difficulties: Easy, Medium, Hard
* [x] Difficulty changes the number of clues played per game
* [x] Game cannot be started until a difficulty is selected
* [x] Difficult select form is reset to default none value after every game
* [x] Added a popup alert that displays the users strike count when a strike occurs
* [x] Game features persistent Round, Win, Loss and Strike counters
* [x] Game has reset button that resets counters so users don't have to refresh page to do so
* [x] Game has dynamic button layout that starts stacked and spreads when game is started
* [x] Clue sequence is replayed after a non-game-ending strike occurs
* [x] Replayed Clue sequences do not decrease the clue hold time, but instead replay at the same interval

## Video Walkthrough (GIF)

If you recorded multiple GIFs for all the implemented features, you can add them here:

The game features a dynamic button layout that stacks and spreads, a difficulty selection form and persistent counters for Round, Wins, Losses and current Strike count:
![](https://i.imgur.com/kUM0RlP.gif)

Users can stop the current game at any point and the round counter will erase that round from the count:
![](https://i.imgur.com/AkSSh9u.gif)

The difficultly selection form resets after each round:
![](https://i.imgur.com/8Qsn8cR.gif)

Clue sequences play faster as the game progresses:
![](https://i.imgur.com/IcTyjB6.gif)

Users can reset the counters using a reset button:
![](https://i.imgur.com/TqH7fa0.gif)


## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 
https://developer.mozilla.org/en-US/
https://stackoverflow.com/
https://www.w3schools.com/
https://www.geeksforgeeks.org/

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words)

One of the challenges that I encountered during this project was getting the difficulty selection to work properly. I knew that I wanted to challenge myself by implementing this feature, but I wasn't entirely sure how to best do so. 
I first had to consider what would make the game more or less difficult and determine how I would change that parameter. Because the game also plays clues at a faster rate as the sequences grow in length, it became clear to me that shortening the maximum length of the random pattern, would in fact make the game easier. 
Therefore I implemented a global variable for the length of the pattern array, so that I could use this variable in a function that sets the length variable and in the function that generates the random array. I also needed to find a solution on how to get a user's selection for their desired difficulty. 
I decided to use a select form for this and use the value returned from that form to set the value of the length variable. Then I could use that value in my random array function to set the number of times the for loop iterates when pushing random integers into the pattern array. 
I also needed to consider what happens if a difficulty is not selected, or if that should be possible. I decided to hide the start button until a difficulty is selected. But this presented a bug that I was stuck on for quite some time. When a game ended, the difficulty select form would not be reset and therefore the same difficulty option could not be selected. 
Further, the ‘Select One’ option could be selected from this point and this would break the game. I needed to find a way to reset my select form and I needed to find a way to prevent the ‘Select One’ default option from being selected. Through research I learned more about the document.getElementById( ) method and used this to set a variable equal to my select form. 
From there I was able to access the properties of the element using .selectedIndex to reset the form drop-down to the 0 index. I also set the 0 index to be the default selected option for the form. Now I just needed to perform these steps in all instances where the game ends.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 

I have a lot of questions remaining about web development. This project gave me the opportunity to learn more about front-end development and the design process involved in creating an interactive application. I’ve taken courses in web development and databases and my focus in those courses has been on the back-end development, such as implementing CRUD functionality using React, Express and MongoDB or MySQL, with a lesser focus on the front-end or client-side experience. 
Therefore, I still have a lot of questions about React and Express and how to create full-stack applications that use databases in meaningful way and that also provide a front-end UI experience that feels modern and professional.  I still have a lot of questions about using CSS and HTML and how to design the front-end’s form and function. I have questions about web design standards and best practices. 
I still have a lot of remaining questions about object-oriented programming in JavaScript, about the promise object and built-in objects in JavaScript. In general, I would like to be more fluent and familiar with JavaScript, CSS and HTML so that I can create more interesting web projects. 
I also think having a deep understanding of databases would be an invaluable skill and I would really like to learn more about advanced data manipulation queries in SQL for example and how they can be used to create better and or more complex functionality. I would also like to get more experience with git, version control, deployment and collaborating on a web development project using a repository. 
I also have questions about web security and how to develop an application that maintains its security. Lastly, I still have questions about debugging in web development and would like to learn more about debugging JavaScript.

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 

The first thing I would want to work on would be optimizing this project for mobile/touchscreen devices. When making this project more unique and adding optional features, I incorporated pictures of my children as I imagined my daughter being able to experience the game, and what fun that would be for her. My daughter is only 2 years old and she doesn’t know how to use a mouse yet. 
This limits her ability to play along. I opened the project in my phone’s browser and noticed that the buttons don’t make sounds or display images when touched and that they’re all in a single column. Therefore you can only see the first few buttons and not all 8 buttons at once. This makes it so you can’t see the clue sequence that plays and you can’t get feedback when buttons are pressed. 
It would be fun to learn how to optimize this project for a touchscreen browser. I think my daughter would really love to be able to play this memory game with pictures of her and her brother, and perhaps showing her that you can make something like this would inspire her creativity. I would also want to work more on the design of the project via the CSS and HTML. 
I would want to spend more time making the UI feel and look more aesthetically pleasing and professional. I spent most of my time in the project programming the JavaScript, and I think improving the UI could give me an opportunity to become more familiar and fluent with CSS and HTML. Other ideas would include: custom audio for the buttons and audio that plays when the game is won/lost, and dynamic images for the buttons that move around after each game.


## Interview Recording URL Link

[My 5-minute Interview Recording](https://www.loom.com/share/7474e499d7724d54a059b48499a7f244)


## License

    Copyright Casey Anderson

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.