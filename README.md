# 🔥 Redis Top Interview Questions

Redis interview question bank for backend and MERN Stack developers, organized by level. Use this list for focused preparation, from fundamentals to production scenarios and advanced Redis concepts.

## 🟢 Level 1 — Must Know Basics

1. **What is Redis?**

   **Interview Answer (English):** Redis is an open-source, in-memory data structure store commonly used as a database, cache, message broker, and streaming engine. It stores data as key-value pairs and supports data structures such as Strings, Hashes, Lists, Sets, Sorted Sets, and Streams. Because data is primarily served from memory, Redis provides very low-latency access. It also supports persistence options such as RDB snapshots and AOF logs to save data to disk.

   **Hinglish Explanation:** Redis ek open-source, in-memory data store hai. Iska matlab data ko primarily RAM mein store aur access kiya jata hai, isliye read/write operations bahut fast hote hain. Hum Redis ko caching, session management, API rate limiting, real-time messaging aur counters jaise use cases mein use karte hain. Redis sirf cache nahi hai—configuration aur use case ke according ise database ya messaging ke liye bhi use kar sakte hain. Data ko disk par save rakhne ke liye RDB aur AOF persistence options available hain.

   **Simple Example (Redis commands):**
   ```redis
   SET user:1 "Amit"
   GET user:1
   ```

   **Output:**
   ```text
   "OK"
   "Amit"
   ```

   **How it works:** `user:1` is the key and `Amit` is the value. `SET` stores the value, and `GET` retrieves it.

   **One-line revision:** Redis is a fast, in-memory key-value/data-structure store used for caching, databases, and messaging, with optional persistence.

2. Why is Redis so fast?
3. Is Redis a database or a cache?
4. What are the main use cases of Redis?
5. How does Redis store data?
6. What are Redis data types?
7. What is a Redis key-value pair?
8. What is TTL in Redis?
9. What is key expiration in Redis?
10. What are the most commonly used Redis commands?
11. Redis vs MongoDB — what's the difference?
12. Redis vs Memcached — what's the difference?
13. When should you use Redis?
14. When should you NOT use Redis?
15. Can Redis be used as a primary database?

## 🟡 Level 2 — Data Types & Commands

16. What is Redis String?
17. What is Redis Hash?
18. What is Redis List?
19. What is Redis Set?
20. What is Redis Sorted Set (ZSet)?
21. String vs Hash in Redis?
22. Set vs Sorted Set?
23. List vs Set?
24. What is the SET command?
25. What is the GET command?
26. What is SETEX?
27. What is EXPIRE?
28. What is TTL?
29. What is DEL?
30. What is INCR / DECR?
31. What are HSET and HGET?
32. What are LPUSH and RPUSH?
33. What are SADD and SMEMBERS?
34. What are ZADD and ZRANGE?
35. What is SCAN and why is it preferred over KEYS?

## 🔥 Level 3 — Caching (Very Important for MERN)

36. What is caching?
37. Why do we use Redis for caching?
38. How does Redis caching work with Node.js?
39. What is the Cache-Aside pattern?
40. What is a Write-Through Cache?
41. What is a Write-Behind Cache?
42. What is a Read-Through Cache?
43. What is a Cache Hit?
44. What is a Cache Miss?
45. What happens when cache expires?
46. How do you set TTL for a cache?
47. How do you invalidate Redis cache?
48. What is cache invalidation?
49. What is cache avalanche?
50. What is cache penetration?
51. What is cache breakdown / stampede?
52. How do you prevent cache avalanche?
53. How do you prevent cache penetration?
54. How do you prevent cache stampede?
55. What data should NOT be cached in Redis?

## 🔴 Level 4 — Persistence

56. Does Redis persist data?
57. What is Redis RDB?
58. What is Redis AOF?
59. RDB vs AOF?
60. Which is faster: RDB or AOF?
61. Which provides better durability: RDB or AOF?
62. Can we use RDB + AOF together?
63. What happens to Redis data after a restart?
64. What is BGSAVE?
65. What is SAVE?
66. What is the difference between SAVE and BGSAVE?

## 🔥 Level 5 — Redis Pub/Sub

67. What is Redis Pub/Sub?
68. Why do we use Redis Pub/Sub?
69. How does Pub/Sub work?
70. What are Publisher and Subscriber?
71. What are PUBLISH and SUBSCRIBE?
72. What is a Redis channel?
73. Redis Pub/Sub vs Kafka?
74. Redis Pub/Sub vs RabbitMQ?
75. What happens if a subscriber is offline?
76. Can Redis Pub/Sub store messages?
77. What is Redis Streams?
78. Redis Pub/Sub vs Redis Streams?

**Important:** Redis Pub/Sub provides real-time broadcasting, but messages are not persisted for offline subscribers. If you need message persistence, replay, or consumer-group processing, consider Redis Streams.

## 🟠 Level 6 — Transactions & Atomicity

79. Does Redis support transactions?
80. What is MULTI?
81. What is EXEC?
82. What is DISCARD?
83. What is WATCH?
84. What is an atomic operation in Redis?
85. Redis transaction vs MongoDB transaction?
86. Can Redis transactions be rolled back?
87. What is optimistic locking in Redis?

**Important:** Redis transactions commonly use MULTI/EXEC, with WATCH available for optimistic locking. Redis transactions do not provide general rollback semantics like some relational database transactions.

## 🔥 Level 7 — High Availability & Scaling

88. What is Redis Replication?
89. What is Primary-Replica architecture?
90. What happens when the Redis primary fails?
91. What is Redis Sentinel?
92. Why do we use Redis Sentinel?
93. Redis Sentinel vs Redis Cluster?
94. What is Redis Cluster?
95. Why do we need Redis Cluster?
96. What is sharding in Redis?
97. How does Redis Cluster distribute data?
98. What are hash slots in Redis Cluster?
99. How many hash slots does Redis Cluster have?
100. What is automatic failover in Redis?
101. How does Redis achieve high availability?
102. Replication vs Sharding?

**Important:** Replication maintains copies of primary data. Sharding distributes data across nodes for horizontal scaling; Redis Cluster combines sharding with primary-replica replication.

## 🔥 Level 8 — Node.js + Redis (Very Important for MERN)

103. How do you connect Redis with Node.js?
104. Which Redis client do you use in Node.js?
105. How do you store JSON data in Redis?
106. How do you retrieve JSON data from Redis?
107. How do you implement API caching using Redis?
108. How do you cache MongoDB query results using Redis?
109. How do you invalidate cache after a MongoDB update?
110. How do you implement Redis session management in Express?
111. How do you store JWT/session data in Redis?
112. How do you implement rate limiting using Redis?
113. How do you implement OTP expiration using Redis?
114. How do you implement a distributed lock using Redis?
115. How do you use Redis with WebSocket/Socket.IO?
116. How do you use Redis Pub/Sub in microservices?
117. How do you handle Redis connection failure in Node.js?
118. What happens if Redis goes down?
119. Should an application fail if Redis is unavailable?
120. How would you design Redis caching in a MERN application?

## 🔥 Level 9 — Advanced / 3–4 Year Experience

121. What is Redis eviction policy?
122. What happens when Redis memory becomes full?
123. What is LRU?
124. What is LFU?
125. What is the noeviction policy?
126. What are Redis eviction policies?
127. How do you monitor Redis memory usage?
128. How do you troubleshoot slow Redis?
129. Why can Redis become slow despite being in-memory?
130. What is a hot key?
131. How do you handle hot keys?
132. What is the big key / large key problem?
133. How do you find large Redis keys?
134. What is pipelining in Redis?
135. Why is Redis pipelining useful?
136. What is Lua scripting in Redis?
137. Why use Lua scripts?
138. What is distributed locking?
139. How would you implement distributed locking with Redis?
140. What is Redlock?

## ✅ Suggested Study Order

1. **Start with Q1–Q35:** Redis fundamentals, data types, and commands.
2. **Prioritize Q36–Q55:** caching patterns and common cache problems for MERN applications.
3. **Study Q56–Q102:** persistence, Pub/Sub, transactions, high availability, and scaling.
4. **Practice Q103–Q120:** Node.js and MERN implementation scenarios.
5. **Prepare Q121–Q140:** memory, performance, locking, and advanced concepts.

## 📝 Answer Format for Future Notes

For each question, prepare:
- **Interview Answer (English):** a clear, concise definition you can say in an interview.
- **Hinglish Explanation:** a simple explanation in your own words.
- **Practical Example:** Redis commands or Node.js code where relevant.
- **Key Difference / Diagram:** when a comparison or architecture makes the concept easier to understand.

---

**Goal:** Build practical Redis knowledge for MERN Stack interviews, including real-world caching, API rate limiting, sessions, Pub/Sub, and production troubleshooting.
