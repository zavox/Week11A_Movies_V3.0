# Java Movies V3.0

In this task you will have to upgrade your Product and Buyable handler application, using serialization and networking. Please, keep in mind: not all the code snippets should be used (e.g. setters and getters), but you have to write them. In this task you will have to create a new class, called ObjectServer, but you will have to be able to run this class as a separated application, so it has to have a main method. This class should be able to send and receive objects over TCP, working as a server (hint: ServerSocket should be initialized in this class). The RentManager and the ObjectServer should communicate with each other using sockets (they should run in separated JVMs). ObjectServer should be able to save given data to a file and load data from file, depends on its mode property, so it should be declared in this class. You should modify your Person class and every product class, because they are needed to be able to read/write with ObjectInputStream/ObjectOutputStream. Create an enum which contains 3 values: GET, PUT and EXIT. Any of these values can be sent to the server which can process these "commands" and switches its mode: GET means the server should read the file which contains the previously stored data and send it to the caller. PUT means the server should be switched to "store" mode, so the data which is sent to the server after PUT command should be stored in a file (PUT command and the data are different objects !!!). EXIT means the server should shut down and the sockets are needed to be closed.

![Movies_UML](objectserver.jpg)