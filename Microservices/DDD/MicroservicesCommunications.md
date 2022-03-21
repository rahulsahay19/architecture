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
