# Java Collection Framework – Interview Notes

This document summarizes important **Java Collection Framework concepts frequently asked in interviews**.

---

# 1️⃣ What is the Collection Framework?

The Java Collection Framework is a **set of interfaces and classes used to store and manipulate groups of objects**.

It provides:

* Data structures
* Algorithms
* Utility methods

---

# 2️⃣ Core Interfaces

| Interface  | Description                    |
| ---------- | ------------------------------ |
| Iterable   | Root interface                 |
| Collection | Base interface for collections |
| List       | Ordered collection             |
| Set        | Unique elements                |
| Queue      | FIFO structure                 |
| Map        | Key-value pair storage         |

---

# 3️⃣ List Implementations

| Class      | Characteristics    |
| ---------- | ------------------ |
| ArrayList  | Dynamic array      |
| LinkedList | Doubly linked list |
| Vector     | Thread-safe list   |
| Stack      | LIFO structure     |

---

# 4️⃣ Set Implementations

| Class         | Characteristics           |
| ------------- | ------------------------- |
| HashSet       | Unordered unique elements |
| LinkedHashSet | Maintains insertion order |
| TreeSet       | Sorted elements           |

---

# 5️⃣ Queue Implementations

| Class         | Characteristics         |
| ------------- | ----------------------- |
| PriorityQueue | Priority based ordering |
| ArrayDeque    | Double ended queue      |

---

# 6️⃣ Map Implementations

| Class         | Characteristics           |
| ------------- | ------------------------- |
| HashMap       | Fast lookup using hashing |
| LinkedHashMap | Maintains insertion order |
| Hashtable     | Thread-safe map           |
| TreeMap       | Sorted key map            |

---

# 7️⃣ Important Differences

## ArrayList vs LinkedList

| Feature       | ArrayList     | LinkedList  |
| ------------- | ------------- | ----------- |
| Structure     | Dynamic Array | Linked List |
| Access        | Fast          | Slow        |
| Insert/Delete | Slow          | Fast        |

---

## HashMap vs Hashtable

| Feature     | HashMap | Hashtable   |
| ----------- | ------- | ----------- |
| Thread Safe | No      | Yes         |
| Null Key    | Allowed | Not Allowed |
| Performance | Faster  | Slower      |

---

# 8️⃣ Why Map is not part of Collection?

Because Map stores **key-value pairs**, while Collection stores **single objects**.

---

# 9️⃣ Internal Working

### HashMap

Uses:

* Hashing
* Buckets
* Linked list / Tree structure

---

### ArrayList

Uses:

* Dynamic array
* Resizing mechanism

---

# 🔟 Interview Tip

Always remember the hierarchy:

```
Iterable
   ↓
Collection
   ↓
List / Set / Queue

Map (Separate hierarchy)
```

---

# Key Takeaway

Understanding the **architecture of the Java Collection Framework** helps developers design **scalable and modular systems**.
