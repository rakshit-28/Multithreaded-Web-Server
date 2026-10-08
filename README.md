# Multithreaded-Web-Server

A simple Java-based collection of socket server examples showing how the same basic client/server interaction can be implemented with different concurrency models.

This repository includes:

SingleThreaded/ — a basic server that accepts one connection at a time
Multithreaded/ — a server that creates a new thread for each client connection
ThreadPool/ — a server that uses a fixed-size thread pool for better resource management
Project Overview
These programs use Java's built-in networking APIs (ServerSocket and Socket) to demonstrate:

socket communication over localhost
basic request/response messaging
single-threaded versus multithreaded server design
thread-pool-based concurrency
Each example is intentionally minimal and educational, making it a useful starting point for learning network programming and Java threading.

Repository Structure
MultithreadedWebServer/
├── SingleThreaded/
│   ├── Client.java
│   └── Server.java
├── Multithreaded/
│   ├── Client.java
│   └── Server.java
├── ThreadPool/
│   └── Server.java
└── README.md
This repository is a small Java networking demo focused on comparing different server concurrency models.

At a high level:

It contains 3 self-contained server implementations:
SingleThreaded
Multithreaded
ThreadPool
Each folder appears to include a Server.java and a Client.java, so each variant is meant to be run and tested independently.
What each variant does:

SingleThreaded: accepts incoming connections one at a time, using a basic ServerSocket loop. It sends a simple greeting to each client.
Multithreaded: creates a new Java thread for each accepted client connection, so multiple clients can be served concurrently.
ThreadPool: uses a fixed-size ExecutorService thread pool instead of creating a new thread per client, which is a more scalable pattern.
The code is very lightweight and educational rather than production-style:

Server listens on port 8010
Clients connect and receive a “Hello…” message from the server
The repo is mainly about demonstrating how server architecture changes when handling concurrent clients
So the repository’s core theme is: “How different threading strategies affect a basic TCP server.”
