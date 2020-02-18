# SQL vs NoSQL or MySQL vs MongoDB
https://www.youtube.com/watch?v=ZS_kXvOeQ5Y

SQL - Relational Data Base - Table Schema Based
  strict Schema Based.
Type of relations: 
  one to one
  one to many
  many to many
  
No-SQL = Mongo DB, AWS Dynamo DB.
  Mongo DB -(Humongous) 
  Data Base = Shop
  Collections(Tables in SQL) = Users and Orders
  Documents (rows/records in SQL) = look like JSON
  Dont Follow Same Schema , rows can have diff schema/columns
  No/Few Relations , keep all required data in same Table/record.
  cause duplicate data, but all is present in same place,so no nned to query on other tables.
  good for more reads, and less write DB.



# ACID versus BASE
https://www.johndcook.com/blog/2009/07/06/brewer-cap-theorem-base/
  - Atomic: Everything in a transaction succeeds or the entire transaction is rolled back.
  - Consistent: A transaction cannot leave the database in an inconsistent state.
  - Isolated: Transactions cannot interfere with each other.
  - Durable: Completed transactions persist, even when servers restart etc.

An alternative to ACID is BASE:
  - Basic Availability
  - Soft-state
  - Eventual consistency
Rather than requiring consistency after every transaction, it is enough for the database to eventually be in a consistent state. (Accounting systems do this all the time. It’s called “closing out the books.”) It’s OK to use stale data, and it’s OK to give approximate answers.
It’s harder to develop software in the fault-tolerant BASE world compared to the fastidious ACID world, but Brewer’s CAP theorem says you have no choice if you want to scale up.
However, as Brewer points out in this presentation(https://people.eecs.berkeley.edu/~brewer/cs262b-2004/PODC-keynote.pdf), there is a continuum between ACID and BASE. You can decide how close you want to be to one end of the continuum or the other according to your priorities.

# Towards Robust Distributed Systems
(https://people.eecs.berkeley.edu/~brewer/cs262b-2004/PODC-keynote.pdf)

Dr. Eric A. Brewer Dr. Eric A. Brewer
Professor, UC Berkeley
Co-Founder & Chief Scientist, Inktomi

