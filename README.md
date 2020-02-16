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
    - Hadoor- HDFS uses Name Node to store File System Meta Data.
    
    
# Proxies vs VPNs | System Design Basics
  https://www.youtube.com/watch?v=02GbEzYgYIc&list=PLtDbS11SJ-Dldyg4AuXtYbssjZJeYS6IR&index=6

Proxies - intermediate Server/MAchine act as middlemen between Client and Web
  - 1. Farward Proxy - send reqest from user to Web
  - 2. Backward Proxy - send responce from servr to web
  Benefit : REquest Filtering, blocking web sites, Caching frequent downloades into proxy server.hide user identity, track and log user activities.
 - does not support websocket??
VPN : virtual Private Networks
 - create a tunnel connection from user to VPN gateway to Private SErvers/Company server.
 - support HTTP,FTP and Websocket
 - encrypt network packet data and request/responce
 
 
# Messaging Queues | System Design Basics
https://www.youtube.com/watch?v=sfQwMu0SCT8&list=PLtDbS11SJ-Dldyg4AuXtYbssjZJeYS6IR&index=7
 1. simple system - Request responce model - synchronous request responce process.
 2. in Distributed system - Asynchronous request responce 
   -  use Publisher- subscriber model , use Message Queues 
    -  Rabbit MQ
    - Zero MQ
    - Kafka MQ
3. Event Driven API mechanism, for buy/sell transaction, inventory consistency
  Microservices Architecture - What are event driven architectures?
  https://www.youtube.com/watch?v=uJ4JFMMbSO8
  

# L16: The CAP Theorem
https://www.youtube.com/watch?v=k-Yaq8AHlFA
trade off between Consistency , Availibility in presence of Partition in you distributed system.




# Monolith vs Microservices | System Design Basics
https://www.youtube.com/watch?v=F8ClTNWgkqY&list=PLtDbS11SJ-Dldyg4AuXtYbssjZJeYS6IR&index=8






