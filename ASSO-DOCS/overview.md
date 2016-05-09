
**BinaryFun**

**Index**

 [Description](#description)
 
  New Features
 
 Software Architecture
 
  .Logical View
 
  [Process View] (#Process)

# ** Description **

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

**New Features**

We decided to add some features to the game in order to make it more complete and to turn it into a client-server application.
We added the feature of multiplayer. This feature would allow us to implement a network package, necessary in client-server applications. 
We added a quit button in the end so the user could quit the application.

# **Process View**

The process view deals with the dynamic aspects of the system, like its processes and how they communicate. The UML Diagram to represent process views include the Activity Diagram. An activity diagram shows the overall flow of control.

In our game the player can choose to participate in a multiplayer mode or a single player mode. After choosing the desired mode the player is presented with a menu and he can choose between tutorials or to pick a game. If the player picks a game, it can be in single or multiplayer mode, he will go into a different section, a Play Zone (the game he chose). After the game is played, a highscore table will appear and the player will have to add he's name.

![Image of GameMode](http://s32.postimg.org/avdiito11/Untitled.png)




Status API Training Shop Blog About
© 2016 GitHub, Inc. Terms Privacy Security Contact Help
