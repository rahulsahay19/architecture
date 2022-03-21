# DDD Bounded Contexts:
One of the best way to design microservices is via DDD. Hence, before jumping to the solution, we should understand bounded context properly.

**Bounded Context**

Below diagram at high level explains the same

![image](https://user-images.githubusercontent.com/3886381/159170213-9c31a137-008f-4c9b-be97-1953e0d45251.png)

DDD divided into two phases.
- **Strategic**:- Here we define large scale model of the system defining to do business rules.

- **Tactical**:- Its mostly focused on implementation and provides design patterns which we can use like Entities, Aggregates, Value Objects, Repositories and Domain Services

Domain driven designs are driven by its own common language which is called **ubiquitous** language and independent units are called bounded contexts.

A complex domains may contain many sub domains. And these sub domains can be grouped together defined by common responsibilities. And, we can say that these groups of sub domains are bounded contexts. A bounded context is a grouping of closely related scopes, which we can say as logical bondaries. 

Like in the diagram we can see that we have two bounded contexts separated by logical boundary. And within this boundary we have sub doains which is fulfilling the same purpose.

## Identification of bounded context

In order to identify bounded context, we should use DDD. And with DDD, we should context mapping pattern for identification of bounded context. With context mapping pattern, we can identify the whole bounded context and the logical boundaries. 

![image](https://user-images.githubusercontent.com/3886381/159223222-22085c0a-c7cb-4a42-88a9-fe1bc653455b.png)

Like as shown above, the diagram can be conceptualized as 

![image](https://user-images.githubusercontent.com/3886381/159223370-b72bb220-a3d1-4f93-ab45-605bdb4d01e4.png)

Then, we can apply domain analysis to model microservices. This will follow the below path.

![image](https://user-images.githubusercontent.com/3886381/159224364-97b030b1-ed39-410a-a0e1-aa8256c88410.png)

## Case Study - Ecommerce Project

In this model, we are going to understand nouns and verbs to analyze ecommerce domain. As part of this exercise, we would to list first our user stories. 

![image](https://user-images.githubusercontent.com/3886381/159224763-97b42c45-10b1-42c5-bfa8-cbf9f578534b.png)

Here, red ones are **verbs** and black ones are **nouns**. Having said that, we can interact with these nouns and verbs with different communication style which we will see later. Once we have figured out nouns and verbs. Next step is to create object interaction diagram.

From the previous diagram, we can easily list nouns like shown below.

- Customer
- Order
- Product
- Category
- Brand
- Address
- User
- Supplier
- Shopping Cart
- Shopping Cart Items 
- Order Details

Based on nouns listed above, here is the diagram which can be sketched out.

![image](https://user-images.githubusercontent.com/3886381/159225695-23999217-f2a9-43e1-b5f6-b76e9ee54b09.png)

Nouns can be translated into entities and then these nouns help creating bounded context based on the interaction diagram. That means these can be further refined into sub domains as well.

## Communication between verbs and nouns

![image](https://user-images.githubusercontent.com/3886381/159226577-d7387e54-c384-4cbd-baa9-5883d9b468b9.png)

# Identifying and Decomposition of Microservices

As you can see below, in the diagram, its bifurcated into multiple categories.

![image](https://user-images.githubusercontent.com/3886381/159227270-fa227547-ba85-4a41-bd08-dca89cd1b832.png)

## Communication between Microservices 

Communication can be of two type. Sync and Async.

- In case of sync, service will have to wait till response come from subequent service and then only it can be proceed.

- In case of async service, things can go parallely, which means request can be fired, that gets queued in some kind of service bus and same will get subsequently processed. Here, subscribers of that service will get notified about the outcome of that.

Therefore, at this stage, Microservices structure looks like this

<img width="1110" alt="image" src="https://user-images.githubusercontent.com/3886381/159231686-72667dba-5eb0-4cf7-973c-70a63c66bf92.png">