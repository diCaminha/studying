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
    1.  Code to sign up a user
    2. Code to list avaliable products
    3. Code to purchase a product
    
    4. code to show products ordered by a particular user

    service 4 requires all other 'services' (1,2 and 3) in order to response the required data. That said, if Service 1 has a problem, then the whole execution of Serrvice 4 will be compromised.

    also another problem is about the time execution. The execution of service 4 is equal to the slowest service (1,2 or 3);


    With Microservices we do this differently: We use a **Event Bus** to handle event notifications (some happened) or receive info.


    
