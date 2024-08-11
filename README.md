# Network chat


## Project description:

1. Two applications for exchanging text messages over the network using a console (terminal) between two or more users.
2. The first application is a chat server, waiting for users to connect.
3. The second application, the chat client, connects to the chat server and delivers and receives new messages.
4. All messages are recorded in file.log on both the server and clients. File.log is updated every time it is launched, as well as every time a message is sent or received. Exit is carried out using the exit command.

# Technologies and libraries:

## Network programming (Java Networking):
Socket: Used on both client and server to establish a connection between them. The client connects to the server using a Socket, and the server accepts connections from clients using a ServerSocket.
ServerSocket: A server side that listens for incoming client connections on a specific port.
## Working with I/O Streams:
BufferedReader and InputStreamReader: Used to read data from the client or server.
PrintWriter and OutputStreamWriter: Used to send data from the client or server.
FileReader and FileWriter: Used to read and write to settings and log files.
## Multithreading:
Thread: To handle simultaneous connections from multiple clients, the server uses multithreading. Each connection is processed in a separate thread using the Runnable interface.
The client side also uses threads to simultaneously send and receive messages.
## Logging:
The code contains its own implementation of a logger, which writes messages with timestamps to the specified file.
The logger uses the Singleton design pattern to provide a single instance of the logger in the entire application.
## Working with configuration files (Properties):
Properties: This class is used to load configuration data (e.g. SERVER_PORT, SERVER_HOST) from the settings.txt file, allowing you to easily configure the server and client.
## Testing:
TestNG: The code contains classes with the @Test annotation, which indicates the use of the TestNG library to write and run tests. Tests check the correct operation of the client and server, as well as the operation of the logger.
## Other:
Scanner: Used on the client side to enter data from the keyboard such as username and messages to be sent to the server.
