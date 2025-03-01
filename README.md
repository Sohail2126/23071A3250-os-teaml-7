Types of IPC Sockets:
Unix Domain Sockets (Local IPC):

Purpose: Primarily used for communication between processes on the same machine.
Advantages:
Faster than network sockets because they bypass the network stack.
No need to worry about network configurations or latency.
They are often used in local server-client communication within the same machine.
Common Uses:
Database Communication: MySQL or PostgreSQL can use Unix domain sockets to allow communication between the database server and client.
Web Server to Application Server Communication: Nginx communicating with PHP-FPM, or a web server communicating with an application server (e.g., Node.js).
Network Sockets (Remote IPC):

Purpose: Used for communication across different machines over a network.
Protocols:
TCP: Reliable, connection-oriented communication.
UDP: Unreliable, connectionless communication.
Advantages:
Communication across different networks or physical machines, allowing distributed applications and services to interact.
Common Uses:
Client-Server Models: Websites where the client (browser) communicates with a server, usually via HTTP or WebSockets.
Microservices: Services deployed across different machines or containers use network sockets to interact, often using protocols like HTTP, gRPC, or WebSocket.
Applications of IPC Sockets:
Database Communication:

Sockets enable fast and reliable communication between database clients and servers.
Local Communication: Typically achieved using Unix domain sockets for performance reasons.
Remote Communication: Over a network using TCP/IP, enabling remote clients to access the database.
Web Servers and Clients:

Web servers (e.g., Apache, Nginx) and application servers (e.g., Node.js, Python Flask) often use sockets for communication.
This could be either local communication via Unix domain sockets or remote communication over the network.
Example: A web server might serve static content, but dynamic content could be processed by an application server through socket-based communication.
Distributed Systems:

Microservices architectures rely heavily on remote IPC to enable services to communicate with each other across a network.
Message Brokers like RabbitMQ or Kafka often use sockets for inter-process communication.
Services might send and receive messages via these brokers using either TCP or UDP sockets.
Message Queues:

RabbitMQ and Redis use network sockets to allow processes to communicate by sending and receiving messages through queues.
RabbitMQ uses AMQP (Advanced Message Queuing Protocol), while Redis might use TCP-based sockets to enable fast, reliable communication in a distributed system.
Real-time Applications:

Applications like online games, video streaming, and chat applications rely on network sockets (usually TCP or UDP) to facilitate real-time data exchange.
WebSockets is a protocol that enables two-way communication over a single TCP connection, often used in real-time web applications, including messaging apps and live feeds.
