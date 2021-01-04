# Aggregate Data Models

The data model describes how we interact with the data in the database; it is the model through which we **perceive** and **manipulate** our data.

It's different from storage model, which describes how the database store the content and manipulates internally. 

The book NoSQL Distilled by Martin Fowler and Pramod J. Sadalage uses the idea of data model to refer to the model by which the database organizes data.

One of the most famous data model is the **relational data model**:
  - set of tables
  - each table contains rows
  - each row represents some entity, that is described by columns attributes with single values.
  - common terminology for tables and rows is relations and tuples.
 
In the NoSQL world, they put away that relational data model, and creates differents data models:
  - key values
  - documents
  - column-family
  - graph

  some of these (key/value, document, column-family) share a common characteristic: aggregate orientation
  
 
## Aggregates

  Key/Value and Document are strongly aggregate-oriented database. They are constructed through aggregates. Both of these types consist of lots of
  aggregates with each aggregate having a key or ID that's used to get the data.
  
  The difference between them is that in a key-value db the aggregate is opaque to the database, so we can't see what really is the aggregate information.
  So we can store anything we want without be worry about types or whatever it is.
  In document, we have types that should be respected by the data used in the aggregation. 
  
  The downside of this for key-value is we can only query bu the key, instead, in a document db, we can submit queries based on the fields in the aggregate,
  we can retrieve part of the aggregate rather than the whole thing. Also the db can create indexes based on the contents of the aggregate.
  
  
