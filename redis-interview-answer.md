# 🔥 Redis Interview Answers

Answers to the questions in [redis-interview-question.md](./redis-interview-question.md). Answer format: English interview definition, Hinglish explanation, practical example, and quick revision.

## 🟢 Level 1 — Must Know Basics

### 1. What is Redis?

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

---

*More answers will be added in question order, using the same format.*
