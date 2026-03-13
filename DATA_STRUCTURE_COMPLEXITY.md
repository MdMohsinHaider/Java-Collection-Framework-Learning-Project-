# Data Structure Complexity Guide

## Overview

This document summarizes the **time complexity, memory usage, and practical use cases of common Java Collection Framework data structures**.

Understanding these helps developers:

* Choose the right data structure
* Optimize application performance
* Improve backend system design
* Prepare for technical interviews

---

# 1️⃣ Time Complexity Table

## List Implementations

| Operation       | ArrayList | LinkedList | Vector |
| --------------- | --------- | ---------- | ------ |
| Access (get)    | O(1)      | O(n)       | O(1)   |
| Add (end)       | O(1)      | O(1)       | O(1)   |
| Insert (middle) | O(n)      | O(1)       | O(n)   |
| Remove          | O(n)      | O(1)       | O(n)   |
| Search          | O(n)      | O(n)       | O(n)   |

---

## Set Implementations

| Operation        | HashSet | LinkedHashSet | TreeSet  |
| ---------------- | ------- | ------------- | -------- |
| Add              | O(1)    | O(1)          | O(log n) |
| Remove           | O(1)    | O(1)          | O(log n) |
| Search           | O(1)    | O(1)          | O(log n) |
| Order Maintained | No      | Yes           | Sorted   |

---

## Map Implementations

| Operation   | HashMap | LinkedHashMap | Hashtable | TreeMap  |
| ----------- | ------- | ------------- | --------- | -------- |
| Put         | O(1)    | O(1)          | O(1)      | O(log n) |
| Get         | O(1)    | O(1)          | O(1)      | O(log n) |
| Remove      | O(1)    | O(1)          | O(1)      | O(log n) |
| Thread Safe | No      | No            | Yes       | No       |

---

## Queue Implementations

| Operation | PriorityQueue | ArrayDeque |
| --------- | ------------- | ---------- |
| Insert    | O(log n)      | O(1)       |
| Remove    | O(log n)      | O(1)       |
| Peek      | O(1)          | O(1)       |

---

# 2️⃣ Memory Usage Comparison

| Data Structure | Memory Usage | Reason                                      |
| -------------- | ------------ | ------------------------------------------- |
| ArrayList      | Low          | Uses contiguous array                       |
| LinkedList     | High         | Each node stores next and previous pointers |
| HashMap        | Medium       | Uses bucket array and nodes                 |
| TreeMap        | High         | Uses tree nodes                             |
| HashSet        | Medium       | Uses HashMap internally                     |

---

# 3️⃣ When to Use Each Collection

## ArrayList

Use when:

* Frequent data access
* Random index access needed
* Mostly read operations

Example:

```java
List<String> users = new ArrayList<>();
```

Common use cases:

* API response lists
* Search results
* UI data tables

---

## LinkedList

Use when:

* Frequent insertions and deletions
* Queue or stack behavior needed

Example:

```java
LinkedList<String> queue = new LinkedList<>();
```

Common use cases:

* Task queues
* Undo/Redo systems

---

## HashSet

Use when:

* Unique elements required
* Fast lookup needed

Example:

```java
Set<String> emails = new HashSet<>();
```

Common use cases:

* Removing duplicates
* Permission checks
* Unique user tracking

---

## TreeSet

Use when:

* Sorted elements required

Example:

```java
Set<Integer> scores = new TreeSet<>();
```

Common use cases:

* Leaderboards
* Ranking systems
* Sorted datasets

---

## HashMap

Use when:

* Fast key-value lookup required

Example:

```java
Map<Integer, String> users = new HashMap<>();
```

Common use cases:

* Database caching
* Session storage
* API data mapping

---

## LinkedHashMap

Use when:

* Order of insertion must be preserved

Example:

```java
Map<Integer, String> cache = new LinkedHashMap<>();
```

Common use cases:

* LRU Cache implementation
* Ordered processing

---

## TreeMap

Use when:

* Sorted key-value storage needed

Example:

```java
Map<Integer, String> leaderboard = new TreeMap<>();
```

Common use cases:

* Ranking systems
* Sorted reports
* Financial data

---

## PriorityQueue

Use when:

* Tasks must be processed based on priority

Example:

```java
PriorityQueue<Integer> pq = new PriorityQueue<>();
```

Common use cases:

* Task scheduling
* Job processing systems
* Shortest path algorithms

---

# 4️⃣ Real Backend Use Cases

## API Data Caching

```java
Map<String, Object> cache = new HashMap<>();
```

Stores frequently accessed API data.

---

## User Session Management

```java
Map<String, UserSession> sessions = new ConcurrentHashMap<>();
```

Tracks active users in web applications.

---

## Removing Duplicate Records

```java
Set<String> uniqueEmails = new HashSet<>();
```

Ensures unique email addresses.

---

## Task Scheduling System

```java
PriorityQueue<Task> taskQueue = new PriorityQueue<>();
```

Processes tasks by priority.

---

## LRU Cache Implementation

```java
LinkedHashMap<Integer, String> cache = new LinkedHashMap<>();
```

Maintains insertion order for cache eviction.

---

# 5️⃣ Key Takeaways

✔ Choose data structures based on **operation complexity**
✔ Understand **memory usage trade-offs**
✔ Use **HashMap / HashSet for fast operations**
✔ Use **TreeMap / TreeSet for sorted data**
✔ Use **LinkedList for frequent modifications**

---

# Final Thought

A strong understanding of **data structure complexity and real-world usage** helps developers design **high-performance backend systems**.

This knowledge is essential for:

* Backend development
* Microservices architecture
* High scalability systems
* Technical interviews
