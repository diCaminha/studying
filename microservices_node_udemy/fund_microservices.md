# What is microservice

## How happens in a monolitc architecture

1. a request goes through an *auth middleware*
2. then it is redirected to **one of many features** by a router
3. the feature executes/gest some data from the *database*
4. the response goes back to the requester


A single microservice contains:
- routing
- middlewares
- business logic
- database access
 to implement **one feature of our app**


 ## Data in Microservices

One of the big challenges when decided to go on a microservice architecture is about the data management between services. 
Once all the features are separated even in different database so we need to create a logic to orchestrate the info among the
many services.

We need different databases for each feature in order to:
- run services/features independently of others
- schema might change
- some services might works better in a specific type of db

We never access data for feature A in a database B. neighter for feature B in db A.

## Communication Strategies: Async and Sync
Sync: services communicate with each other using direct requests
Async: services communicate with each other using **events**

A problem with using Sync communication:
ex: 
    we have 4 services:
    Service 1.  Code to sign up a user
    Service 2. Code to list avaliable products
    Service 3. Code to purchase a product
    
    Service 4. code to show products ordered by a particular user

    service 4 requires all other 'services' (1,2 and 3) in order to response the required data. That said, if Service 1 has a problem, then the whole execution of Serrvice 4 will be compromised.

    also another problem is about the time execution. The execution of service 4 is equal to the slowest service (1,2 or 3);


    With Microservices we do this differently: We use a **Event Bus** to handle event notifications (some happened) or receive info.


## Pros and Cons of Async communication
A first advantage would be that Service 4 has zero dependency on other services! We might say that the dependency of Service 4 on the others is an indirect dependency, since the service 4 can still answer requests even if all other services are down.

As a 'problem' for async would be the amount of data duplication. But, the amount to pay is not that relevant value. So we're fine to duplicate data and pay for the extra data.

You might say that it's harder to understand, and that's the second point of 'cons' for async comunication.


