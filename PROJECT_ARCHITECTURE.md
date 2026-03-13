# Project Architecture

## Overview

This project recreates the **Java Collection Framework architecture** to understand how real frameworks are designed.

It focuses on:

* Interface-based design
* Separation of abstraction and implementation
* Modular package structure

---

# Core Architecture

The framework is divided into two main hierarchies:

1. Collection Hierarchy
2. Map Hierarchy

---

# 1️⃣ Collection Hierarchy

```
Iterable
   ↓
Collection
   ↓
List
Queue
Set
```

Each of these interfaces defines a **specific data structure behavior**.

---

# List Hierarchy

```
MyList
  │
  ├── MyArrayList
  ├── MyLinkedList
  ├── MyVector
  └── MyStack
```

### Characteristics

* Ordered collection
* Allows duplicates
* Index based access

---

# Queue Hierarchy

```
MyQueue
   │
   ├── MyPriorityQueue
   └── MyDeque
          │
          └── MyArrayDeque
```

### Characteristics

* FIFO structure
* Element processing order

---

# Set Hierarchy

```
MySet
  │
  ├── MyHashSet
  ├── MyLinkedHashSet
  └── MySortedSet
        │
        └── MyTreeSet
```

### Characteristics

* No duplicate elements
* Unique value storage

---

# 2️⃣ Map Hierarchy

The Map hierarchy is separate from Collection.

```
MyMap
  │
  ├── MyHashMap
  ├── MyLinkedHashMap
  ├── MyHashTable
  └── MySortedMap
        │
        └── MyTreeMap
```

### Characteristics

* Stores key-value pairs
* Key must be unique

---

# Design Principles Used

### 1. Abstraction

Interfaces define behavior.

Example:

```java
public interface MyCollection {
    void add(Object obj);
}
```

---

### 2. Implementation Separation

Classes implement the interfaces.

Example:

```java
public class MyArrayList implements MyList {
}
```

---

### 3. Hierarchical Design

Each interface specializes the behavior of the parent interface.

---

# Learning Benefits

This project helps developers understand:

* Framework design patterns
* Interface hierarchy
* Data structure abstraction
* API design
* Real Java framework architecture
