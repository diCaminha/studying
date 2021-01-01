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

  
