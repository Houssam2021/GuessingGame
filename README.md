# GuessingGame
#### Video Demo:  <https://www.youtube.com/watch?v=OIM0FwWGpj0>
#### Description: This app starts with a starting page (or activity) contains 2 buttons that start mini guessing games:
## Starting page:
#### Displays the icon of the app in the center of the screen, and two buttons that start the guessing games and under each button a reference for the previous score that gets saved even if the new score is higher or lower than the previous one.
### - Files that helped the creation of the starting screen:
#### *Activity_main2.xml*: Helps with the look of the starting screen. Using the ConstraintLayout, I positioned the icon, buttons and the texts that represent the previous score of the player. Plus, giving them IDs, text size, color, length, width and default text for each View.
#### *MainActivity2.java*: Handles the interaction with the player. For example, it takes every View (everything the user sees on screen) by their id (almost same concept as HTML, CSS) and changes their attribute: it gives each button an "OnClick listener" to start the chosen game. And takes the last score from a chosen game and displays it on this screen (under the chosen game's button).
#### *strings.xml*: saves anything that's in form of string and displays it in its given/proper location.
## Guess where's the country:
#### In this mini game the player is given a world map, and on it some radio buttons are displayed, the country's name on the bottom of the map and on top of the map the question counter (6 questions in total), additionally, a count down timer (30 seconds) located on the top right corner, To let the player guess faster.
### - Files that helped the creation of "Guess where's the country":
#### *activity_guessing_countries.xml*: Using ConstraintLayout, I positioned the map, radiogroup, radio buttons, score, question counter, timer and name of the country to be guessed in the proper positions. Plus, giving them IDs, text size, color, length, width and default text for each View.
#### *Question.java*: a Java class with a constructor of all the options off the radio buttons.
#### *guessing_countries.java*: Makes each View interactive. creates an ArrayList of type Question (using the Question.java class from earlier) and makes a method that adds the countries names in this ArrayList. 
#### Gives an OnClick method that checks if the answer is true (add a point) or false (removes a point) and changes the score, all that by making a method called "checkAnswer". 
#### "nextQuestion" method is created to change the question.
#### "startTimer" method that starts the timer and changes its color to red whenever the player is running out of time (whenever the timer gets to 10 seconds).
#### "Send" method sends the score to the MainActivity2 so that it displays as previous score.
#### onSaveInstanceState/onRestoreInstanceState method saves the score during gameplay even when the user flips the phone.
## Guess the Animal
#### In this mini game, the player is given an image of an animal, below it 4 buttons with options, on top let corner the score, on top right corner the timer (25 seconds each round). The player will guess the animal and press on of the buttons representing his answer: If it's true the player earns 2 , else, the player loses 1 point. Either way, continues playing the game until he answered all of them (10 in total).
### - Files that helped the creation of "Guess the animal": 
#### *activity_guessing_animal*: Using ConstraintLayout, I positioned the image, score, timer, and the 4 buttons in the proper positions. Plus, giving them IDs, text size, color, length, width and default text for each View.
#### *Data.java*: a Java class with 2 arrays "animals" (for the images) and "answers" (answers for each image written in the same order as the animals array elements).
#### *AnimalItem*: a Java class representing an animal, with a constructor of all name and image of each animal.
#### *guessing_animals*: handles the interactivity. Has a List of type AnimalItem (using the AnimalItem.java class from earlier) using a for loop, I add all animals' images and name.
#### Collections.shuffle(list) that makes the questions shuffle each playthrough.
#### OnClick listener for each button, True answer-> +2 and a Toast message that says "Correct!", False answer-> -1 and a Toast message that says "INCORRECT!", then gets to the next question using a method called "newQuestion" that randomises the buttons positions each round.
#### "startTimer" method that starts the timer and changes its color to red whenever the player is running out of time (whenever the timer gets to 10 seconds) used to reset the timer for each round.
#### onSaveInstanceState/onRestoreInstanceState method saves the score during gameplay even when the user flips the phone.
