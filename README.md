# Custom Java Collection Framework (Learning Project)

## 📌 Overview

This project is a **custom implementation of the Java Collection Framework hierarchy** created for learning and understanding how real Java frameworks are designed internally.

The project replicates the **structure of Java Collections** including interfaces and classes such as:

* Iterable
* Collection
* List
* Queue
* Set
* Map

The purpose of this project is to understand **framework design, interface hierarchy, and abstraction in Java**.

---

## 🎯 Learning Objectives

This project helps developers understand:

* How Java frameworks are structured
* Interface-based architecture
* Inheritance and implementation relationships
* Separation of API and implementation
* Framework design principles

---

## 🧠 Collection Framework Hierarchy

```
Iterable
   │
   └── Collection
        │
        ├── List
        │    ├── ArrayList
        │    ├── LinkedList
        │    ├── Vector
        │    └── Stack
        │
        ├── Queue
        │    ├── PriorityQueue
        │    └── Deque
        │          └── ArrayDeque
        │
        └── Set
             ├── HashSet
             ├── LinkedHashSet
             └── SortedSet
                    └── TreeSet


Map (Separate Hierarchy)
   │
   ├── HashMap
   ├── LinkedHashMap
   ├── HashTable
   └── SortedMap
         └── TreeMap
```

---

## 📂 Project Structure

```
com.mohsin.collectionframework
│
├── iterable
│   └── MyIterable.java
│
├── collection
│   └── MyCollection.java
│
├── list
│   ├── MyList.java
│   ├── MyArrayList.java
│   ├── MyLinkedList.java
│   ├── MyVector.java
│   └── MyStack.java
│
├── queue
│   ├── MyQueue.java
│   ├── MyPriorityQueue.java
│   └── deque
│       ├── MyDeque.java
│       └── MyArrayDeque.java
│
├── set
│   ├── MySet.java
│   ├── MyHashSet.java
│   ├── MyLinkedHashSet.java
│   └── sortedset
│       ├── MySortedSet.java
│       └── MyTreeSet.java
│
└── map
    ├── MyMap.java
    ├── MyHashMap.java
    ├── MyLinkedHashMap.java
    ├── MyHashTable.java
    └── sortedmap
        ├── MySortedMap.java
        └── MyTreeMap.java
```

---

## ⚙️ Technologies Used

* Java
* Object Oriented Programming
* Interface-based Design
* Package Structure

---

## 🚀 How to Run

1. Clone the repository

```bash
git clone https://github.com/yourusername/custom-java-collection-framework.git
```

2. Open in IDE (IntelliJ / Eclipse / VS Code)

3. Run the classes to understand how interfaces and implementations work.

---

## 📖 Example Concept

Example interface hierarchy:

```java
public interface MyCollection extends MyIterable {

    void add(Object obj);

    void remove(Object obj);

    int size();

    boolean isEmpty();
}
```

Example implementation:

```java
public class MyArrayList implements MyList {

    @Override
    public void add(Object obj) {
        System.out.println("Element added in ArrayList");
    }
}
```

---

## 🔥 Future Improvements

Planned improvements for deeper framework understanding:

* Generic Collection Framework (`<T>`)
* Dynamic Array Implementation
* Custom Iterator Implementation
* Internal HashMap Implementation
* Real Data Structure Logic
* Unit Testing

---

## 👨‍💻 Author

**Md Mohsin Haider**

Java Full Stack Developer
Passionate about **framework design, backend development, and system architecture**.

---

## ⭐ Contribution

This project is mainly for **educational purposes**.
Feel free to fork and experiment with the framework structure.

---

## 📜 License

This project is open-source and free to use for learning purposes.
