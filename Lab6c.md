# Memory
```java
class Student {
    String name;
    int age;

    // Method stored in Method Area
    void display() {
        System.out.println("Name: " + name + ", Age: " + age);
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student();   // Object created in Heap
        s1.name = "Alice";            // Instance field in Heap
        s1.age = 20;                  // Instance field in Heap

        s1.display();                 // display() method called
    }
}
```
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



# instance block & static block

## 1. Static Block

- Runs **only once** — when the class is loaded.
- Executed **before `main()`** or **before any object of the class is created**.
- **Cannot access instance variables** or use `this` — there is no object context.
- Can access **static variables** and call **static methods**.
- A class can have **multiple static blocks**, executed in the **order they appear**.

**Example:**
```java
class Car {
    static {
        System.out.println("Static block is invoked");
    }
    // only once when class loaed - class level
}
```

---

## 2. Instance Block

- An **instance block** (also called an **initializer block**) is a block of code inside a class **without the `static` keyword**.
- Runs **every time an object is created**, **before the constructor**.
- Can access **instance variables** directly.

**Example:**
```java
class Car {
    {
        System.out.println("Instance block is invoked");
    } // every time object created - obj level
}
```

