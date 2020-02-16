# Distributed-Computing
Distributed Computing

# Load Balancing
https://www.youtube.com/watch?v=FUkjEQYJ0Bc&list=PLtDbS11SJ-Dldyg4AuXtYbssjZJeYS6IR&index=1
What is Load Balancing | System Design Basics

Various load balancing algorithm examples such as 
  - round robin , 
  - IP hashing (ip address hashing) 
  - meta data (no of active coonection, bandwidth speed, responce time). 


# Consistance Hashing
  https://www.youtube.com/watch?v=ffE1mQWxyKM&list=PLtDbS11SJ-Dldyg4AuXtYbssjZJeYS6IR&index=5
  1. Normal Hashing - Hash the Partiion Key , then % modulus with No of DB present, to find target DB PArtition to store/Retrive Data.
if more DB added or deleted, then we need to REdistribute DB and Hash-Modulo Function will keep changing 
  2. Consistent Hashing - Hashed value of Request mapped into a ring , HASH(KEy), Key = Request ID / DB Primary key ID / IP Address.  
    - Server No also mapped into Ring, 
    - add / delete DB cause only 1  neighbour change
    - or add multiple Virtual Serve node into Ringh by hasing 1 server ip with multiple hash functions and map 1 server's multiple Virtual Nodes at diff location in Ring.

# Caching in Web Application
https://www.youtube.com/watch?v=joifNgoXXFk&list=PLtDbS11SJ-Dldyg4AuXtYbssjZJeYS6IR&index=2

  - Web server saves DB data into Inmemory Cache Ex. Redis In memory Cache.
  - for multiple server nodes we can have their own In memory cache ( cause duplictes more cache miss vs cache hit)
  - Distributed cache, with consistent Hashing, and load balancer.
  - Global Cache - causes single point failure, bottleneck
  - another type of cache - CDN - Content Distribution Network Cache, with Web server sharing Static Content (html,css,js,media files) via DB.
  
 Cache Coherent - When Data gets updated in DB, then cache and DB has different data, data inconsistency .
 how to handle chche coherency: on Data Write 3 approaches:
 1. Write Through - update both Chche and DB on single Update Request, but Write Time increases
 2. Write Around - update only DB not Cache
 3. Write Back - Only Update Cache not DB.
 
 Cache Eviction Policy :
 1. First In First Out vs Last in First Out
 2. Lease Recently Used vs Most Recently Used
 3. Least Frequently Used or Most Frequently Used
 4. Random Replacement.
 
 
 
# Sharding & Database Partitioning | System Design Basics
https://www.youtube.com/watch?v=RynPj8C0BXA&list=PLtDbS11SJ-Dldyg4AuXtYbssjZJeYS6IR&index=4

Data Base Partitioning - divid data to multiple DB , can be implemnted at 2 places Application level or DataBase Level
1. Application Level Data Base Sharding:
  - MemCache DB and 
  - Redis DB - both are In Memory DB Caching
2. Database Level Sharding supported by 
  - Mongo DB.
  - Cassandra 
  - Apache HBASE 
  - Hadoop - HDFS DB

Data Base PArtitioning Methods
  1. Vertical Partitioning
    - Tweeter (User profile,Tweets, Liked/Favourites, friends are stoded in diff DBs)
  2. Horizontal Partitioning
    - Slack , (diff DB store company Starting with A,B ... )

Data Partitioning Criteria 
  1. Algorithmic Sharding
    - Sharding Function - like Hashing, Consistent Hashing , Used By MemCache.
  2. Dynamic Sharding
    - has Global Lookup Table
    - Mongo DB stores, Config Server to store this information
    - Hadoor- HDFS uses Name Node to store File System Meta Data.https://www.youtube.com/watch?v=ffE1mQWxyKM&list=PLtDbS11SJ-Dldyg4AuXtYbssjZJeYS6IR&index=5
    
  

  

 
 










