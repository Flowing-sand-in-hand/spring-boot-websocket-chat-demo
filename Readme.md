## Spring Boot WebSocket Chat Appplication

You can checkout the live version of the application at https://spring-ws-chat.herokuapp.com/

![App Screenshot](screenshot.png)

## Requirements

1. Java - 11

2. Maven - 3.x.x

## Steps to Setup

**1. Clone the application**

```bash
git clone https://github.com/callicoder/spring-boot-websocket-chat-demo.git
```

**2. Build and run the app using maven**

```bash
cd spring-boot-websocket-chat-demo
mvn package
java -jar target/websocket-demo-0.0.1-SNAPSHOT.jar
```

Alternatively, you can run the app directly without packaging it like so -

```bash
mvn spring-boot:run
```

## Learn More

You can find the tutorial for this application on my blog -

https://www.callicoder.com/spring-boot-websocket-chat-example/

## Using this project to learn WebSocket

This project is a great resource for learning WebSocket with Spring Boot. It demonstrates how to set up a WebSocket server, handle WebSocket messages, and create a simple chat interface. By studying the code and running the application, you can gain a solid understanding of WebSocket concepts and how to implement them in a Spring Boot application.

## WebSocket Configuration

The WebSocket configuration is done in the `WebSocketConfig.java` file. This file configures the WebSocket endpoints and the message broker. The `registerStompEndpoints` method registers the `/ws` endpoint, which clients will use to connect to the WebSocket server. The `configureMessageBroker` method configures the message broker with application destination prefixes and enables a simple in-memory broker.

## WebSocket Message Handling

The WebSocket message handling is done in the `ChatController.java` file. This file contains methods to handle WebSocket messages. The `sendMessage` method handles messages sent to the `/chat.sendMessage` destination and broadcasts them to the `/topic/public` destination. The `addUser` method handles messages sent to the `/chat.addUser` destination and adds the user to the WebSocket session.
