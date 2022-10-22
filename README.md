# Project Dcumentation
https://docs.google.com/document/d/1JvGs3MdVSd9Pmhjs2qwSehwicMjsZaDGJ86qB_eEVb0/edit?usp=sharing

## Unity Version -2020.3.32f1

## Quest Project 

This is a very simple quest project. 

There are 2 kinds of quests- 

## Prime Number Quests-
The user can start a Prime Number quest, where he has to enter a given amount of integers or whole numbers within a given time( default 10s). On entering the given amount of correct prime numbers, the quest is over.

## Composite Number Quests-
Similar to prime number quest, where the user has to enter a given amount of composite numbers.

All quests can run independent of each other,and can be active at the same time.

## How To Play

1.)Press Start Prime No Quest/ Start Composite No Quest to initialize the respective quest. The button OnClick() event attached to it contains an integer argument, which is the amount of prime/ composite numbers to be entered. Any number of quests of any type can be started at any time.

2.)Important thing to note here is that each quest has a Quest Id( can be seen in the player gameobject’s component in the inspector).

3.)The Set Quest TO Enter To button is used to decide which quest the user wants to enter numbers to (by default it will enter to questID 0).. The OnClick() event of this button contains integer argument that can be used to set the questId to which numbers are to be entered.

4.)Numbers can be entered to the quests by then pressing the Enter Number button. The OnClick() event of the button has an integer argument that will be entered on pressing the button.
If the set quest is a Prime Number quest, only prime numbers will be accepted as entries, and wrong entries will be shown in the debug console.. Same for Composite Number quest.

5.)After a quest has started, the quest can be monitored on the Inspector of the Player gameobject in the hierarchy. The GameManger script is attached to the Canvas.

Completing each quest increases the player’s level by 1. Failing quests decreases the player’s level by if it is greater than 0. The time limit for the quest can be changed from the exposed variable in the GameManager script attached to the Canvas.

## IMPORTANT NOTE: 
To enter numbers to quests, please set the questId of the desired quest by setting the integer argument of the Set Quest To Enter To button, and then PRESS the button to set the questId. 
Please make sure to PRESS the button to set the questId.

## Class descriptions

Quest- Quest related attributes and methods are defined here. 

Player- Contains information about the current player and keeps track of all quests and related variables.

GameManager- Contains logic to initialize quests, and handle events when the quest is completed.

MathCalculations- Utility class for math calculations



