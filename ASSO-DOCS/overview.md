
<h1>BinaryFun</h1>

**Index**

[Description](#description)

[New Features](#new-features)
 
Software Architecture:
 
  [Logical View](#logical-view)
 
 [Process View](#process-view)
	 
 [Implementation View](#implementation-view)
	 
 [Deployment View](#deployment-view)
	 
 [Use Case View](#use-case-view)

## Description
BinaryFun is an Android Application game that has an educational purpose.

![Image of Application](http://imageshack.com/a/img922/580/9fKEHJ.png)

When you open this application you have access to game modes such as Binary Adder, Binary to Decimal, Binary to Hexadecimal and Boolean Fun.
The games consist in timed exercises in which you a have to make calculus, depending on the game mode you choose. 

![Image of Binary Adder](http://imageshack.com/a/img921/6862/9FkPuk.png)

There is a score and a table of high scores.

![Image of Highscore Table](http://imageshack.com/a/img922/6553/I1QOQ2.png)

If you have any doubts about the games you can access Learn Binary, Learn Logic, Learn Arithmetic and Learn Representations for more explanations and help.

![Image of Learn](http://imageshack.com/a/img922/5359/MyYr4S.png)

Since it's an Android Application it is implemented in Java, lessons view are made by HTML and css and it uses Gradle to build the project. 
To run it you need an Android envoirenment, like a smartphone with a software version Android API 21, also known as Lollipop.
To compile the whole project you need 
	
	internal_impl-22.0.0.jar

	classpath 'com.android.tools.build:gradle:1.1.0'
	
which are the libraries of gradle to build the project and an android's library.


The description of the commits show us what functionalities have been added or what problems were fixed.
To make a commit you have to fork the original repository. When you make a change that is usefull to the project you make a pull request and the ''master'' decides if he wants to add your changes to the project or not.



To us it is a simple application and anyone can play its games. There are no major issues.

## New Features

We decided to add some features to the game in order to make it more complete and to turn it into a client-server application.
We added the feature of multiplayer. This feature would allow us to implement a network package, necessary in client-server applications. 
We added a quit button in the end so the user could quit the application.

## Logical View

The Logical View describes the internal structure of our system, the integrated parts and their relations.
The UML Diagrams allow us to do a model of the view of the system. We will use a Class Diagram to do so.

A class represents a group of objects with similar behaviour and caractheristics. 
Within a class have atributes and methods, atributes represent a propriety of a class defined by abstract terms and methods can modify the values of the atributes and change its status.

Instead of the original code, we decided to implement the multiplayer feature and to do that we would need a new initial menu so the user could choose to play multiplayer or singleplayer from the initial point of the application. We "created" two new classes designated **SinglePlayer** and **MultiPlayer** that would inherit all the methods that would create an event or activity from the **MainActivity** class.

The classes **LearnBinary**, **LearnRepresentations**, **LearnLogic** and **LearnArithmetic** refer to the tutorials.

The classes **BooleanFun**, **BinaryToDecimal**, **BinaryAdder** and **BinaryToHex** refer to a game mode, that when finished saves the score of the player by executing the class **SaveScore**, which, if it's a highscore, will save it in the **Highscore** class which is a table.

![Image of LogicalView](http://s32.postimg.org/4jy9jiyud/Logical_View.png)

## Process View

The process view deals with the dynamic aspects of the system, like its processes and how they communicate. The UML Diagram to represent process views include the Activity Diagram. An activity diagram shows the overall flow of control.

In our game the player can choose to participate in a multiplayer mode or a single player mode. After choosing the desired mode the player is presented with a menu and he can choose between tutorials or to pick a game. If the player picks a game, it can be in single or multiplayer mode, he will go into a different section, a Play Zone (the game he chose). After the game is played, a highscore table will appear and the player will have to add he's name.

![Image of GameMode](http://s32.postimg.org/67ggvaced/Untitled.png)

## Implementation View

Implementation View can be represented by a Component Diagram and describes system components. It shows us how the software interacts with the user.

In the game application the Main loads all the Libraries to launch the game. Once the game is running the player has to choose a PlayerMode (SinglePlayer or MultiPlayer). Afterwards has to pick a game and in the end of the game the player can submit his score to the HighScore table which is connected locally if the player chose SinglePlayer otherwise it is connected to a server.

![Image of Implementation View] (http://s32.postimg.org/nrk58ixvp/implementation_1.jpg)

## Deployment View

The Deployment View models the physical aspects of the application. We have artifacts and nodes, each representing the software part and the hardware part respectively.

In SinglePlayer Mode we have the Client node and the Database node. 

In MultiPlayer Mode exists two Players nodes, who are instances of the node Client that communicates with the Server node. Some information flows directly between the players. 

To store data about highscores a Database is used connected to the Server.

![Image of Deployment View] (http://s32.postimg.org/jvd4k6y85/deployment.jpg)

## Use Case View

The Use Case View allow us to identify the actions that the user can make throughout the application.

In BinaryFun the user can perform several actions like choose a PlayerMode, view some tutorials, choose a GameMode and enter his score in the end of the game. 

![Image of Use Case] (http://s32.postimg.org/d2wkmi4at/usecase.jpg)

Status API Training Shop Blog About
© 2016 GitHub, Inc. Terms Privacy Security Contact Help
