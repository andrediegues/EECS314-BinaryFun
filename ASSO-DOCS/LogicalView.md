**Logical View**

The Logical View describes the internal structure of our system, the integrated parts and their relations.
The UML Diagrams allow us to do a model of the view of the system. We will use a Class Diagram to do so.

A class represents a group of objects with similar behaviour and caractheristics. 
Within a class have atributes and methods, atributes represent a propriety of a class defined by abstract terms and methods can modify the values of the atributes and change its status.

Instead of the original code, we decided to implement the multiplayer feature and to do that we would need a new initial menu so the user could choose to play multiplayer or singleplayer from the initial point of the application. We "created" two new classes designated **SinglePlayer** and **MultiPlayer** that would inherit all the methods that would create an event or activity from the MainActivity class.

![Image of LogicalView](http://s32.postimg.org/9prcwczj9/Logical_View.png)
