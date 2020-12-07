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