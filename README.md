# Java-MultiChat

Java-MultiChat is a chat client and server application written in Java. It allows multiple clients to connect to a server and send messages to each other.

## Features
- User login and logoff
- Send messages to other users
- Notification when users go online or offline

## Getting Started

### Prerequisites

This application requires Java to be installed on your machine.

### Running the Server

1. Run the `MultiThreadServer` main method to start the server.
2. The server will start listening on port 8818 for incoming client connections.

### Running the Client

1. Run the `ChatClient` main method to start a client.
2. The client connects to the server on "localhost" and port 8818 by default.
3. Once connected, the client attempts to login with the username "guest" and password "guest". If successful, the client sends a message to "adam" with the content "Hello!".

## How it Works

### Login

The client sends a command to the server in the format "login [username] [password]". The server then checks if the username and password match. If they do, the server sends a response back to the client saying "you're online" and the client logs in.

### Messaging

The client sends a command to the server in the format "msg [recipient] [message]". The server then forwards the message to the intended recipient.

### Logging Off

The client sends a command to the server saying "logoff" to disconnect from the server.

### Handling Messages

When the client receives a message from the server, it parses the message. If the message starts with "online", "offline", or "msg", it calls the appropriate handler method.
