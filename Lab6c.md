# Memory
## 1. Method Area

* Stores **class bytecode** and **method code** (e.g., `display()`).  
* Shared by all `Student` objects.

```text
Method Area:
 └─ Class: Student
     └─ Method: display()
```
Key Idea:

* All Student objects share the same display() method in memory.

* Only one copy exists for the class.

## 2. Heap

Stores object instances and their instance fields.
```
Heap:
 └─ Object#1: Student (s1)
      ├─ name → "Alice"
      └─ age  → 20
```
Key Idea:

* Each Student object has its own copy of fields (name and age).

* Multiple objects will each have separate fields in the Heap.

## 3. Stack

Stores local variables and method call frames.
```
Stack:
 └─ main() frame
     ├─ local variable: s1 → reference to Object#1

 └─ display() frame (when s1.display() is called)
     ├─ hidden parameter: this → Object#1
```
Key Idea:

* Local variables like s1 store references to objects in Heap.

* When a method is called, a new frame is created on the stack with this pointing to the object.

## 4. Visual Summary
| Memory Area   | Stores                                     |
|---------------|-------------------------------------------|
| Method Area   | Class definitions & method code           |
| Heap          | Object instances & instance fields        |
| Stack         | Local variables & method call frames      |



