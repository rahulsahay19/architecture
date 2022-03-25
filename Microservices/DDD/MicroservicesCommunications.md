# Microservices Communication

Monolithic: In case of monolithic applications, communication between modules will **inter-process comunnication**. 

Microservices: In case of Microservices, communication will be inter service communication. In this case, network calls will be distributed in nature. However, there can be different protocols involved as shown below.
- HTTP
- GRPC
- Message Brokers
- AMQP 

And the same can be applied synchronusly or asynchronusly. Below Diagram higlights the same.

![image](https://user-images.githubusercontent.com/3886381/159232320-8e17bdb7-7982-40a6-a87d-40f144bd6f81.png)

## Different kind of communications

![image](https://user-images.githubusercontent.com/3886381/159234586-5a6f9594-7df3-41c0-9a07-fc3ffeee6a66.png)

Synchronous communication can be used to return sync responses based on HTTP protocol or GRPC protocol. Here, client sends the request and wait for the response which means client call will block the thread until reponse comes.

Another communication type is Asynchronous communication. Here client will send the request and won't wait for the response. It will continue with next tasks. Means here, IO is not blocked. These are of different types like

- AMQP (Advanced Messaging Queuing Protocol)
- One To One (Queue)
- One to Many (Topic)
- PUB/SUB 
- Event Driven

## Designing HTTP based Restful APIs for MicroServices

For seqential calls, we should focus on Restful designs. It basically follows following HTTP Verbs like GET, POST, PUT, Patch. We should also keep these things in mind while designing the api.

- Avoid chatty calls
- What should be public APIs meant for gateway
- What shpuld be private APIs meant for backend 
- REST Vs GRPC protocols

![image](https://user-images.githubusercontent.com/3886381/159731081-ea129a1c-3bf4-4724-ba8f-79c56e6d0b1f.png)

Sample diagram illustrates the same.

## REST Features
- Stateless
- Uniform Interface
- Cacheable
- Client-Server
- Layered System
- Code on Demand

# GRPC

- Based on Remote Procedure Calls developed at google.
- It uses HTTP/2 protocol to transport binary messages.
- Protocol buffers aka Protobuf files
- Cross Platform client and server bindings

# How GRPC works

![image](https://user-images.githubusercontent.com/3886381/159735705-31989a94-a33e-4d31-8d19-0cbefc269285.png)

- In GRPC, a client application can directly call a method on server application on a different machine like a local object.

- Its become very handy protocol for building distributed applications and services.

- Here, we define a servuce that specifies methods which can be called remotely.

- This can be written in any language which GRPC supports.

# Advantages of GRPC

- Using HTTP/2 protocol
- Binary Serialization
- Multi language platform support
- Open source and backed by google
- Supports Bi-directional streaming operations.

# GRPC vs REST

![image](https://user-images.githubusercontent.com/3886381/159737286-159039bc-2fb2-44f4-a854-3179fe256996.png)

# Usage of GRPC in Microservices environment

- Synchronous backend microservice to microservice communication
- Polyglot environments
- Point to Point real time communication
- Low latency and high throughput communication
- For Payload constraints requirements, it fits well as it takes very less space.

# Sample example of GRPC communication

![image](https://user-images.githubusercontent.com/3886381/159738585-aca09ff3-bdec-46a0-912e-5ac4cba7717a.png)

# Asynchronous Message Based Communication

- This is the case where multiple services need to interact with each other.
- Without any dependency and at the same time it has to be loosely coupled.
- Message based communication
- Eventual consistency
- Message broker systems
- AMQP Protocol
- Kafka, RabbitMQ, Azure Service Bus are few examples

## Type of Commuication

![image](https://user-images.githubusercontent.com/3886381/160139910-01986096-887d-4fff-9310-c8a202bf08cb.png)

One to many example. This works on pub/sub model. This is widely used in event based architecture where in there are many subscribers to one publisher, which makes it ideal for the case of 1...N

- Here there is one Event Bus Interface
- Where in order gets submitted as event
- Then subscriber picks that up and processes the same
- In Event-driven architecture, CQRS pattern, event storing, eventual consistency gets applied

![image](https://user-images.githubusercontent.com/3886381/160140351-d076135a-e7c5-4e37-96d3-70881a7c833b.png)

## Dependency Inversion Principle (DIP)

![image](https://user-images.githubusercontent.com/3886381/160142269-8d910361-f39c-410a-bcb9-6ace05599564.png)

This is the general thumb rule which gets applied everywhere.

## Pub/Sub Pattern (Publish-Subscribe)

![image](https://user-images.githubusercontent.com/3886381/160142658-8873d62b-41ea-44f1-a240-237e6efc2e75.png)
