# AutoClean

Welcome to AutoClean. Number 1 autonomous world cleaner in the world
in this project we implemented the basic infrastructure for the world cleaner robot. 

this was done by different modules we will elaborate about.

![Alt Text](assets/Driver.gif)
# sql database
the center of all data transmission. all modules commuinicate with the sql server by writing and reading from it when needed.
this way we create modularity in our software and we create an easy environment for future development.
the sql server is Azure SQL Edge which runs on the ubuntu of the TX2 nvidia device via docker. We are using it for sensors and driver module use cases such as driver need to operate based on sensors information or driver need to execute a driving command. The SQL database holds those commands and sensors info in different tables and all the modules communicate through them.
# sensors
this module is all about getting the info from the pixhawk(sensors device) and deliver it to the sql server
# driver
the driver modules gets a string of driving instructions which he can parse. those instructions are coming from the instructions list in the sql db
this way we can control the driving while creating the base for future module to send the instructions itself.
# communication
this module role is to be the mediator between groundstation and the world cleaner. also if needed to communicate between devices on robot itself


