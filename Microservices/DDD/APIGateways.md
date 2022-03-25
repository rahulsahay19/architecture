# API Gateways

Before jumping into API Gateways, let's understand the problems with direct client to microservices communication.

- Chatty Communications
- Increased latency and complexity on UI
- Client try to handle multiple calls
- Direct Backend APIs get exposed
- Exposes fine grained endpoints

![image](https://user-images.githubusercontent.com/3886381/159747826-d68c65a3-3072-45ca-906e-c77dd084da2d.png)

Above diagram explaining direct communication pattern. These problems solved using API Gateways as shown below in the diagram.

![image](https://user-images.githubusercontent.com/3886381/159748283-a96911a5-3533-47f8-b0ca-e6f4e4f0085f.png)

## Features of API Gateway

- It can handle cross cutting concerns like security, authorization etc
- Routing to internal microservices
- Aggregate several microservices

## API Gateway Patterns

There are three types of API Gateway.

- Gateway Routing pattern
- Gateway Aggregation pattern
- Gateway offloading pattern

## Gateway Routing Pattern

Gateway routing pattern routing requests to multiple microservices. Basic features are listed below.

- Exposes a single endpoint.
- Layer 7 routing
- Protocol abstraction
- Centralized Error Management

## Gateway Aggregation Pattern

This is similar to routing pattern explained above plus some added benefits.

- It aggregate multiple internal requests and respond with one request.
- This means, that it reduces chattiness.
- This improves network performance by cutting down the number of calls

## API Gateway Pattern

- This is largely suited for building complex microservices.
- This is very much like facade pattern as explained in OOPs.
- This acts as reverse proxy or gateway routing for communicating to internal microservices
- Routing requests from client to backend services
- Only cons is single point of failure risk. In order to avoid this we can keep backup of gateway 

## Features of API Gateway Pattern

This can be explained via ocelot(Gateway library for .Net)
- Routing
- Authentication
- Request Aggregation
- Authorization
- Service Discovery with Consul and Eureka
- Throttling
- Load Balancing
- Logging
- Tracing
- Correlation Pass-Through
- Headers Transformation
- Query Transformation
- Quality of Service
- Custom Middleware

## Backends for Frontends Pattern (BFF)

- Separate API Gateways for different User Interfaces. Say a mobile experience needs a cutdown experience, hence it can follow a separate track
- It also solves Single point of failure
- Avoid bottleneck on one gateway

Below diagram explains the same

![image](https://user-images.githubusercontent.com/3886381/159757397-1a9bdaae-a4d9-4ea6-9fcd-276e711859eb.png)

## Service to Service Communications

Generally HTTP/GRPC communication happens between service to service. It depends on the nature of requirement. But, we should try to avoid as much call between services as it increases latency. In this case, it follows Request/Response sync messaging pattern.

# Service Aggregator Pattern

- It minimizes service to service communication.
- It receives the request from API gateway and dispatches the same to multiple backend services and combines the result and then return the result.

Below diagram explains the same.

![image](https://user-images.githubusercontent.com/3886381/159760544-8e248c25-e996-41df-a7ed-c3309f6b7c0d.png)

# Service Registry Pattern

In this case, microservices register itself with service registry so that other microservice or gateway can discover the service and send the request.

![image](https://user-images.githubusercontent.com/3886381/160130756-75396616-760a-40b5-bc49-de5f4db9651b.png)

Here many instances of differen services are running. Therefore, what gateway will do, it will pick one of the available instances of these services 