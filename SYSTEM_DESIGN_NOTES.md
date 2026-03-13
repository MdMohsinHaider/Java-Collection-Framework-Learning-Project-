# System Design Notes – Java Collection Framework

## Overview

This document explains the **internal design and working principles of core Java Collection Framework data structures**.

Understanding these internals helps developers:

* Write optimized code
* Choose the correct data structure
* Design scalable systems
* Perform well in technical interviews

---

# 1️⃣ ArrayList – Internal Design

## Structure

ArrayList internally uses a **dynamic array**.

```
Index → 0   1   2   3   4
        ─────────────────
Data  → A | B | C | D | E
```

Internally:

```java
Object[] elementData;
```

---

## Dynamic Resizing

When the array becomes full:

```
Old Capacity = 10
New Capacity = 10 + (10 / 2) = 15
```

Growth formula:

```
newCapacity = oldCapacity + (oldCapacity >> 1)
```

---

## Time Complexity

| Operation       | Complexity |
| --------------- | ---------- |
| Access          | O(1)       |
| Add (end)       | O(1)       |
| Insert (middle) | O(n)       |
| Remove          | O(n)       |

---

## Advantages

* Fast random access
* Memory efficient

## Disadvantages

* Slow insert/delete in middle

---

# 2️⃣ LinkedList – Internal Design

## Structure

LinkedList uses **doubly linked nodes**.

```
NULL ← [A] ⇄ [B] ⇄ [C] ⇄ [D] → NULL
```

Node structure:

```java
class Node {
    Object data;
    Node next;
    Node prev;
}
```

---

## Time Complexity

| Operation | Complexity |
| --------- | ---------- |
| Access    | O(n)       |
| Insert    | O(1)       |
| Delete    | O(1)       |

---

## Advantages

* Fast insertions
* No shifting required

## Disadvantages

* Higher memory usage
* Slow random access

---

# 3️⃣ HashMap – Internal Design

HashMap uses **hashing and buckets**.

## Structure

```
Bucket Array
────────────────────────
0 → NULL
1 → [Node]
2 → [Node] → [Node]
3 → NULL
4 → [Node]
```

Each bucket contains a **linked list or tree**.

---

## Hash Calculation

```
index = hash(key) % capacity
```

Example:

```
capacity = 16
hash(key) = 45

index = 45 % 16 = 13
```

---

## Collision Handling

When two keys generate the same index:

```
Bucket[5]

[Node1] → [Node2] → [Node3]
```

After Java 8:

If bucket size > 8 → converted to **Red-Black Tree**.

---

## Time Complexity

| Operation | Average | Worst |
| --------- | ------- | ----- |
| Put       | O(1)    | O(n)  |
| Get       | O(1)    | O(n)  |
| Remove    | O(1)    | O(n)  |

---

# 4️⃣ HashSet – Internal Design

HashSet internally uses **HashMap**.

Example:

```java
HashMap<E, Object>
```

Dummy value used:

```
map.put(element, PRESENT);
```

Structure:

```
Element → Key
Value → Dummy Object
```

---

# 5️⃣ TreeSet – Internal Design

TreeSet uses **Red-Black Tree**.

Properties:

* Self balancing binary search tree
* Sorted order maintained

Example structure:

```
        50
       /  \
     30    70
    / \   / \
  20  40 60 80
```

---

## Time Complexity

| Operation | Complexity |
| --------- | ---------- |
| Add       | O(log n)   |
| Remove    | O(log n)   |
| Search    | O(log n)   |

---

# 6️⃣ Queue – Internal Design

Queue follows **FIFO (First In First Out)**.

```
Front → A → B → C → D → Rear
```

Operations:

```
enqueue()
dequeue()
peek()
```

---

# 7️⃣ Deque – Internal Design

Deque means **Double Ended Queue**.

```
Front → A → B → C → Rear
```

Supports:

```
addFirst()
addLast()
removeFirst()
removeLast()
```

---

# 8️⃣ PriorityQueue – Internal Design

PriorityQueue uses **Binary Heap**.

Structure:

```
        10
       /  \
     20    30
    /  \
  40   50
```

Properties:

* Parent node is smaller than children
* Implemented using array

---

## Time Complexity

| Operation | Complexity |
| --------- | ---------- |
| Insert    | O(log n)   |
| Remove    | O(log n)   |
| Peek      | O(1)       |

---

# 9️⃣ Map vs Collection

| Feature  | Collection    | Map              |
| -------- | ------------- | ---------------- |
| Stores   | Single Object | Key-Value Pair   |
| Examples | List, Set     | HashMap, TreeMap |

Map is **not part of Collection hierarchy**.

---

# 🔟 Choosing the Right Data Structure

| Requirement        | Best Choice       |
| ------------------ | ----------------- |
| Fast search        | HashMap           |
| Sorted data        | TreeMap / TreeSet |
| Frequent insertion | LinkedList        |
| Fast random access | ArrayList         |
| Unique elements    | HashSet           |

---

# Key Takeaway

A strong understanding of **data structure internals and system design principles** helps developers build **efficient and scalable backend systems**.

This knowledge is essential for:

* Backend engineering
* High-performance applications
* Technical interviews
* Framework development
