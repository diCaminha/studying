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