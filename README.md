# Mini Redis — Java

A Redis-like key-value server built from scratch in Java.

The goal of this project is to understand how a simple backend infrastructure system works internally by building the core components myself instead of relying on existing frameworks or libraries.

The project will gradually evolve from a simple in-memory key-value store into a TCP server capable of handling multiple clients, supporting key expiration, persistence, and eventually deployment on AWS EC2.

## 🚀 Project Goals

Through this project, I want to get practical experience with:

* Java Collections
* Hash-based data structures
* Object-Oriented Programming
* Multithreading
* Concurrency
* TCP/IP and Java Sockets
* Client-server architecture
* File persistence
* JDBC & PostgreSQL
* Maven
* JUnit
* Linux
* AWS EC2

## 🛠️ Planned Features

The project will be developed in multiple stages.

### Stage 1 — In-Memory Key-Value Store

* [ ] Key-value data storage
* [ ] `SET` command
* [ ] `GET` command
* [ ] `DEL` command
* [ ] Command parser
* [ ] Console-based interaction

### Stage 2 — TCP Server

* [ ] TCP socket server
* [ ] Client-server communication
* [ ] Multiple simultaneous clients
* [ ] Thread-based request handling
* [ ] Maven project setup
* [ ] Unit testing with JUnit

### Stage 3 — Expiration & Persistence

* [ ] `EXPIRE` command
* [ ] Automatic key expiration
* [ ] Concurrent data handling
* [ ] File-based persistence
* [ ] Explore PostgreSQL/JDBC for snapshots

### Stage 4 — AWS Deployment

* [ ] Deploy the server on an AWS EC2 instance
* [ ] Configure the required networking
* [ ] Run the server on Linux
* [ ] Connect to the server from another machine
* [ ] Test the deployed system

## 📋 Commands

The planned command interface will include:

```text
SET key value
GET key
DEL key
EXPIRE key seconds
```

Example:

```text
SET username abhi
GET username

abhi

EXPIRE username 60
```

The command set will expand as the project develops.

## 🏗️ Architecture

The architecture will evolve throughout the project.

Initial architecture:

```text
Client / Console
       |
       v
 Command Parser
       |
       v
 In-Memory Key-Value Store
       |
       v
 Concurrent Data Structure
```

Later:

```text
Client 1 ──┐
Client 2 ──┼──> TCP Server ──> Command Parser
Client 3 ──┘                       |
                                   v
                            Key-Value Store
                              /         \
                             /           \
                       Expiration      Persistence
                                           |
                                           v
                                      File / PostgreSQL
```

## 🧠 Why I Am Building This

Instead of only building another CRUD application, I wanted to build something that forces me to understand what happens underneath a backend system.

This project gives me an opportunity to work with:

**Java → Networking → Threads → Concurrency → Data Structures → Databases → Linux → AWS**

I also expect to encounter bugs and design problems along the way. Those problems are part of the project.

## 📈 Progress

### Stage 1

🚧 In progress

### Stage 2

⏳ Planned

### Stage 3

⏳ Planned

### Stage 4

⏳ Planned

I will update this README as new functionality is implemented.

## 🔮 Future Ideas

Possible improvements after the core project is complete:

* Better command protocol
* Connection handling improvements
* Graceful server shutdown
* More robust persistence
* Performance benchmarking
* Load testing
* Logging and monitoring
* Additional Redis-like commands

## 👨‍💻 Author

Built as a hands-on Java backend project to understand networking, concurrency, data structures, and backend infrastructure.
