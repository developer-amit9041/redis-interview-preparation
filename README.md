# Redis Interview Preparation

A structured Redis interview question bank for backend and MERN Stack developers. Start with fundamentals, then move through data structures, performance, persistence, scaling, and Node.js integration.

> **Answer format for the study notes:** English interview definition first, followed by a simple Hinglish explanation and practical examples where useful.

## Table of Contents

- [1. Redis Fundamentals](#1-redis-fundamentals)
- [2. Redis Data Types and Commands](#2-redis-data-types-and-commands)
- [3. Expiration, Eviction, and Memory](#3-expiration-eviction-and-memory)
- [4. Persistence, Replication, and High Availability](#4-persistence-replication-and-high-availability)
- [5. Transactions, Lua, and Atomicity](#5-transactions-lua-and-atomicity)
- [6. Pub/Sub, Streams, and Messaging](#6-pubsub-streams-and-messaging)
- [7. Caching Strategies and Cache Problems](#7-caching-strategies-and-cache-problems)
- [8. Performance, Security, and Operations](#8-performance-security-and-operations)
- [9. Redis Cluster and Scaling](#9-redis-cluster-and-scaling)
- [10. Node.js / Express / MERN Integration](#10-nodejs--express--mern-integration)
- [11. Scenario-Based and Advanced Questions](#11-scenario-based-and-advanced-questions)
- [Quick Revision](#quick-revision)

---

## 1. Redis Fundamentals

1. What is Redis?
2. Why is Redis so fast?
3. Is Redis a database, cache, or message broker?
4. What does in-memory data storage mean?
5. Is Redis single-threaded?
6. What changed in Redis 6 and later regarding I/O threading?
7. What are the main use cases of Redis?
8. What is the difference between Redis and a traditional relational database?
9. Redis vs MongoDB: what are the differences?
10. Redis vs Memcached: when would you use each?
11. What are Redis keys and values?
12. What is a Redis database index?
13. What is the default Redis port?
14. What is the Redis CLI, and how do you connect using `redis-cli`?
15. What do `PING`, `INFO`, `DBSIZE`, and `FLUSHDB` do?
16. What is the difference between `FLUSHDB` and `FLUSHALL`?
17. What is the difference between `KEYS` and `SCAN`?
18. How does Redis handle concurrent client requests?
19. What is the Redis event loop?
20. When should Redis not be used?

## 2. Redis Data Types and Commands

21. What data types does Redis support?
22. What is a Redis String, and what are its common use cases?
23. How do `SET`, `GET`, `MSET`, and `MGET` work?
24. What are `INCR`, `INCRBY`, `DECR`, and `APPEND` used for?
25. How do you set a key with an expiration time using `SET`?
26. What is a Redis Hash?
27. What is the difference between a Hash and a JSON string stored in a key?
28. How do `HSET`, `HGET`, `HMGET`, `HGETALL`, and `HDEL` work?
29. What is a Redis List?
30. What are `LPUSH`, `RPUSH`, `LPOP`, and `RPOP`?
31. How can Redis Lists implement a basic queue?
32. What is a Redis Set?
33. How are Sets different from Lists?
34. What do `SADD`, `SREM`, `SISMEMBER`, and `SMEMBERS` do?
35. How do Set operations `SINTER`, `SUNION`, and `SDIFF` work?
36. What is a Sorted Set (ZSET)?
37. How do `ZADD`, `ZRANGE`, `ZRANK`, and `ZSCORE` work?
38. How can Sorted Sets implement a leaderboard?
39. What is a Redis Stream?
40. What is a Bitfield, and when would you use bit operations?
41. What are HyperLogLog and probabilistic counting?
42. What is the Redis Geospatial data type?
43. What are Redis key naming conventions and namespacing?
44. What does `TYPE` tell you about a key?
45. What is the difference between `DEL` and `UNLINK`?

## 3. Expiration, Eviction, and Memory

46. What is key expiration in Redis?
47. What are `EXPIRE`, `PEXPIRE`, `TTL`, and `PTTL`?
48. What does a TTL value of `-1` or `-2` mean?
49. How do `EXPIREAT` and `PEXPIREAT` differ from `EXPIRE`?
50. What happens to the TTL when a key is overwritten or updated?
51. How does Redis expire keys internally?
52. What is the difference between lazy expiration and active expiration?
53. What is a Redis eviction policy?
54. Explain `noeviction`, `allkeys-lru`, `volatile-lru`, `allkeys-lfu`, and `volatile-ttl`.
55. What is the difference between LRU and LFU?
56. What are `maxmemory` and `maxmemory-policy`?
57. What happens when Redis reaches its memory limit?
58. How do you inspect memory usage for a key?
59. What causes Redis memory fragmentation?
60. How can Redis memory usage be reduced?

## 4. Persistence, Replication, and High Availability

61. What is Redis persistence?
62. What is an RDB snapshot?
63. What is AOF (Append Only File)?
64. RDB vs AOF: what are the trade-offs?
65. What does the `appendfsync` setting control?
66. What is AOF rewrite?
67. How can RDB and AOF be enabled together?
68. What data-loss risks exist with different persistence settings?
69. What is Redis replication?
70. What are primary-replica (formerly master-slave) replication and replication lag?
71. Is Redis replication synchronous or asynchronous by default?
72. What is Redis Sentinel?
73. How does Sentinel perform monitoring and failover?
74. Redis Sentinel vs Redis Cluster: what is the difference?
75. What happens to client connections during a failover?
76. What is high availability in Redis?
77. What is split-brain, and why is it a concern?
78. What do `WAIT` and replication acknowledgements help with?
79. What is a Redis backup strategy?
80. How do you restore Redis from an RDB or AOF file?

## 5. Transactions, Lua, and Atomicity

81. What is a Redis transaction?
82. How do `MULTI`, `EXEC`, `DISCARD`, and `WATCH` work?
83. Does Redis provide rollback for every command error in a transaction?
84. What is optimistic locking in Redis?
85. How does `WATCH` help prevent lost updates?
86. What does atomicity mean in Redis?
87. How is a Lua script executed in Redis?
88. What are the benefits and risks of server-side Lua scripts?
89. What is the difference between pipelining, transactions, and Lua scripting?
90. How would you implement a safe counter or inventory decrement?

## 6. Pub/Sub, Streams, and Messaging

91. What is Redis Pub/Sub?
92. Why do we use Redis Pub/Sub?
93. How does Redis Pub/Sub work internally at a high level?
94. What are publishers and subscribers?
95. What do `PUBLISH` and `SUBSCRIBE` do?
96. What is a Redis channel?
97. Redis Pub/Sub vs Kafka: what are the main differences?
98. Redis Pub/Sub vs RabbitMQ: when would you use each?
99. What happens if a subscriber is offline when a message is published?
100. Does Redis Pub/Sub guarantee delivery or persist messages?
101. What is pattern subscription using `PSUBSCRIBE`?
102. What are Redis Streams, and how are they different from Pub/Sub?
103. How do `XADD`, `XREAD`, and `XRANGE` work?
104. What is a Redis Stream consumer group?
105. What do `XREADGROUP`, `XACK`, and `XPENDING` do?
106. How can unacknowledged Stream messages be recovered?
107. When should you choose Pub/Sub, Streams, Kafka, or RabbitMQ?
108. How can Redis support real-time notifications or chat events?

## 7. Caching Strategies and Cache Problems

109. What is caching, and why use Redis as a cache?
110. What is cache-aside (lazy loading)?
111. What is read-through caching?
112. What is write-through caching?
113. What is write-behind (write-back) caching?
114. What is cache invalidation, and why is it difficult?
115. What is a cache hit ratio?
116. What is a cache stampede or thundering herd?
117. How can you prevent a cache stampede?
118. What is cache penetration?
119. What is cache breakdown for a hot key?
120. What is cache warming?
121. How do you keep MongoDB data and Redis cache consistent?
122. What is the difference between cache TTL and database TTL?
123. When should cache entries be invalidated after a write?
124. Should every database query be cached?
125. How would you design caching for a product listing or user profile?

## 8. Performance, Security, and Operations

126. How do you troubleshoot high Redis latency?
127. What does the `SLOWLOG` command show?
128. How do `LATENCY` diagnostics help?
129. What are `INFO`, `MONITOR`, and `CLIENT LIST` used for?
130. Why can `KEYS *` be dangerous in production?
131. What is pipelining, and how does it improve performance?
132. What is the trade-off of sending too many pipelined commands?
133. What is a connection pool, and why is it useful?
134. What can cause Redis timeouts?
135. What are big keys and hot keys?
136. How do you find and handle big keys?
137. How do you secure Redis with authentication and ACLs?
138. Why should Redis not be exposed publicly without protection?
139. What are TLS and network restrictions used for?
140. How do you monitor Redis memory, CPU, connections, and hit rate?
141. What metrics should be monitored in production?
142. How do you perform Redis upgrades with minimal downtime?
143. What is the impact of long-running commands on Redis latency?
144. How should you handle Redis connection failures in an application?
145. What is Redis benchmarking, and how can `redis-benchmark` help?

## 9. Redis Cluster and Scaling

146. What is Redis Cluster?
147. Why do we need Redis Cluster?
148. What are hash slots in Redis Cluster?
149. How does Redis map keys to hash slots?
150. What are hash tags such as `user:{42}:profile`?
151. What are the benefits and limitations of hash tags?
152. How does sharding work in Redis Cluster?
153. What is the difference between replication and sharding?
154. How are slots redistributed during resharding?
155. What do `MOVED` and `ASK` errors mean?
156. What happens if a cluster node fails?
157. What are the minimum practical node and replica considerations for production?
158. What limitations apply to multi-key operations in Redis Cluster?
159. How does a Redis client discover cluster topology?
160. When would you choose a single Redis instance, Sentinel, or Cluster?

## 10. Node.js / Express / MERN Integration

161. How do you connect Node.js to Redis using the `redis` npm package?
162. How do you configure and reuse a Redis client in Express?
163. How do you store and retrieve JSON data in Redis?
164. How do you implement a cache-aside helper in Node.js?
165. How do you set a TTL while caching a MongoDB result?
166. How do you invalidate Redis cache when a MongoDB document changes?
167. How do you implement API rate limiting with Redis?
168. How can `INCR` and `EXPIRE` be used for a simple rate limiter?
169. Why can a naive rate limiter have race conditions?
170. How can Lua scripting make rate-limiter operations atomic?
171. How do you implement sessions using Redis?
172. How can Redis store OTPs or temporary verification codes safely?
173. How do you publish and subscribe to Redis channels from Node.js?
174. Why should publisher and subscriber clients be separated where required by the client library?
175. How do you handle Redis reconnects and connection errors in Node.js?
176. How should an application behave if Redis is unavailable?
177. How can Redis support Socket.IO scaling across multiple Node.js instances?
178. What does the Socket.IO Redis adapter do, and what does it not do?
179. How can Redis support queues and background jobs in a Node.js application?
180. What Redis-related security and configuration values belong in environment variables?

## 11. Scenario-Based and Advanced Questions

181. Redis is fast locally but slow in production. How would you diagnose it?
182. Redis memory is growing continuously. How would you investigate?
183. Your API is returning stale cached data. How would you fix it?
184. Redis has reached `maxmemory`. What happens next, and what would you do?
185. A very popular key overloads one Redis node. How would you handle the hot key?
186. Many requests miss the cache for the same key at once. How do you prevent a stampede?
187. Redis restarts and some cached values disappear. Is this expected?
188. An application loses its Redis connection. How should it recover?
189. Two requests decrement the same product inventory at the same time. How would you avoid overselling?
190. You need to broadcast live updates but do not need message history. Which Redis feature fits?
191. You need to process events after a worker reconnects. Would Pub/Sub be enough?
192. A worker processes a Stream message but crashes before acknowledgement. What happens?
193. How would you build a distributed rate limiter for several API servers?
194. How would you store online-user presence for a real-time chat application?
195. How would you design a Redis-backed leaderboard?
196. How would you cache MongoDB aggregation results?
197. How would you choose a TTL for different categories of data?
198. How would you migrate from a single Redis instance to Redis Cluster?
199. How would you choose between Redis, MongoDB, Kafka, and RabbitMQ in an architecture?
200. Explain a production use case where you used Redis, including trade-offs and failure handling.

---

## Quick Revision

| Topic | Remember |
|---|---|
| Redis | In-memory data structure server used for caching, data access, and messaging |
| String / Hash / List / Set / Sorted Set | Choose the data structure that matches the operation |
| TTL | Controls how long a key remains before expiration |
| Eviction | Determines which keys can be removed when memory is constrained |
| RDB / AOF | Snapshot-based vs append-only persistence approaches |
| Replication | Copies data from a primary to replicas |
| Sentinel | Monitoring and automatic failover for non-clustered Redis deployments |
| Cluster | Sharding and availability across multiple nodes |
| Transactions / Lua | Useful for grouping operations and implementing atomic server-side logic |
| Pub/Sub | Live broadcast; disconnected subscribers miss messages |
| Streams | Persisted ordered entries with consumer groups and acknowledgements |
| Cache-aside | Read cache; on miss read database, then populate cache |
| Cache stampede | Many concurrent requests recompute the same missing/expired value |
| Pipelining | Reduces network round trips by batching commands |
| Production safety | Monitor latency, memory, hit rate, connections, persistence, and failures |

## Suggested Study Order

1. Fundamentals and data structures (Q1–Q45)
2. Expiration, persistence, replication, and transactions (Q46–Q90)
3. Pub/Sub, Streams, caching, and performance (Q91–Q145)
4. Cluster and Node.js integration (Q146–Q180)
5. Scenario-based questions (Q181–Q200)

**Note:** This repository begins with the full question bank. Detailed answers can be added section by section, with English definitions first and Hinglish explanations plus practical examples.
