# WS Introduction

Consumer Application   <---http---> Provider Application

## Interoperability: 
different application built in different languages communicating with each other.
ex: python api talking to a java api

## Loosely Coopled:
If our service A is communicating with service B to get some task from it, and we want to change the provider of that content, we can
easily put C in the place of B and everything is fine.

## Extensibility:
Others can use of our application and extend to other funcionality in their services.

## Mashups:
We can integrate with lots of services, building a mashup system.


## SOAP
It uses XML and HTTP (POST) to communication between services over the web.

## RESTful
It uses multiples formats (XML, JSON, plain text) using the HTTP methods GET, POST, PUT, DELETE...

## Java web services standards
- SOAP --> JAX-WS
- REST --> JAX-RS
