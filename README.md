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
 
 
 
 










