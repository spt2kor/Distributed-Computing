5 Day Learning Challenge - Learn Spring and Spring Boot 
https://courses.in28minutes.com/p/5-day-learning-challenge-get-started-with-spring-and-spring-boot


Big Data Hadoop Tutorial Videos
https://www.youtube.com/playlist?list=PL9ooVrP1hQOFrYxqxb0NJCdCABPZNo0pD

Resilient Distributed Datasets - Apache Spark - RDD
https://www.tutorialspoint.com/apache_spark/apache_spark_rdd.htm

Gossip Protocol used in consistent hashing - IMP
https://www.consul.io/docs/internals/gossip.html

# Making Gossip More Robust with Lifeguard  - IMP
https://www.hashicorp.com/blog/making-gossip-more-robust-with-lifeguard/
  Collectively called Lifeguard, these extensions reduce by 50x the false positives produced by the failure detector and allow us to detect true failures faster.

  Distributed systems such as 
  - BitTorrent, 
  - Apache Cassandra, 
  - Microsoft Orleans, and 
  - HashiCorp Consul commonly use Gossip protocols. 

  They are typically embedded to provide features such as 
  - cluster membership (who is in the cluster), 
  - failure detection (which members are alive), and 
  - event broadcast.

  Their peer to peer nature often makes them much more scalable and reliable than centralized approaches to solving the same problem. 

# Gossip Protocol / SWIM Protocol Overview
https://www.serf.io/docs/internals/gossip.html

# Lamport timestamps
https://en.wikipedia.org/wiki/Lamport_timestamps
  The algorithm of Lamport timestamps is a simple algorithm used to determine the order of events in a distributed computer system. As different nodes or processes will typically not be perfectly synchronized, this algorithm is used to provide a partial ordering of events with minimal overhead, and conceptually provide a starting point for the more advanced vector clock method.
  
  In pseudocode, the algorithm for sending is:
    //event is known
    time = time + 1;
    //event happens
    send(message, time);
    
  The algorithm for receiving a message is:
    (message, time_stamp) = receive();
    time = max(time_stamp, time) + 1;

# Vector clock
https://en.wikipedia.org/wiki/Vector_clock





