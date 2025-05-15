# Codtech_Task3

*COMPANY* : CODTECH IT SOLUTUINS

*NAME* : SHLOK GOYAL

*INTERN ID* : CT04DN206

*DOMAIN* : JAVA PROGRAMMING

*DURATION* : 4 WEEKS

*MENTOR* : NEELA SANTOSH


*DESCRIPTION* -
This Java project is a simple Client-Server Chat Application that allows multiple clients to connect to a server and exchange messages in real time. It demonstrates core concepts of network programming in Java, such as socket communication, multithreading, and stream handling. The application is divided into two main components: the ChatServer and the ChatClient.

The ChatServer class is responsible for listening to incoming client connections using a ServerSocket on port 12345. It uses a Set to keep track of all connected clients through their output streams (PrintWriter), allowing it to broadcast incoming messages to all users. When a new client connects, the server spawns a new thread (ClientHandler) dedicated to handling communication with that client. This enables the server to support multiple clients simultaneously, with each client being managed on its own thread. Inside each thread, the server reads messages from the connected client using a BufferedReader and then broadcasts those messages to all other connected clients using the list of PrintWriter objects. This broadcast functionality is synchronized to avoid concurrency issues, as multiple threads may try to write to clients at the same time.

The ChatClient class represents the client-side of the application. It connects to the server using a Socket and creates input and output streams to read user input and send messages to the server. Upon successfully connecting, the client launches a separate thread to listen for messages from the server so that it can display them in real time while also allowing the user to type new messages. This is done using a lambda expression to create a new thread that continuously reads and prints messages received from the server. Meanwhile, the main thread of the client handles user input from the console and sends it to the server using the output stream.

The design of this chat system ensures real-time communication between multiple clients. Any message typed by a user is instantly broadcasted to all other connected users, creating a group chat environment. The use of multithreading is essential here, as it allows both the server and each client to handle reading and writing operations simultaneously without blocking each other.

This project is a great example for beginners and intermediate learners who want to understand how client-server models work, how to manage multiple connections, and how to implement threaded communication in Java. It also introduces important networking concepts like TCP sockets, streams, and concurrency handling.

To run this project, first start the server (ChatServer), which will wait for incoming connections. Then, run multiple instances of the client (ChatClient) in separate terminals or IDE windows. Each client can send and receive messages in real time. The application can be further enhanced by adding features like user names, private messaging, chat history, and a graphical user interface (GUI).

Overall, this project provides hands-on experience with networking and concurrent programming in Java and forms the basis for more advanced applications like multiplayer games, collaborative tools, and distributed systems.
