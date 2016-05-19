**Deployment View**

The Deployment View models the physical aspects of the application. We have artifacts and nodes, each representing the software part and the hardware part respectively.

In SinglePlayer Mode we have the Client node and the Database node. 

In MultiPlayer Mode exists two Players nodes, who are instances of the node Client that communicates with the Server node. Some information flows directly between the players. 

To store data about highscores a Database is used connected to the Server.


![Image of Deployment View] (http://s32.postimg.org/jvd4k6y85/deployment.jpg)
