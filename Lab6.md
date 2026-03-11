

# 1. Class & Object

A **class is a blueprint**.

```java
class Student {

}
```
### Creating an Object

An object is an instance of a class.
```java
public class Main {
    public static void main(String[] args) {

        Student s1 = new Student();

        System.out.println("Student object created");
    }
}
```
* Student → class definition

* s1 → object created from the class
# 2. Variables (Attributes)
Variables store the data of an object.

Add attributes to the class:
```java
class Student {

    String name;
    int age;

}
```
### Using the Variables
* Variables store object data.
```java
public class Main {
    public static void main(String[] args) {

        Student s1 = new Student();

        s1.name = "Alice";
        s1.age = 20;

        System.out.println(s1.name);
        System.out.println(s1.age);
    }
}
```
* Attributes represent the state of an object

* Each object can store its own data


| Term      | Definition                           | Scope / Notes                      | Example                             |
| --------- | ------------------------------------ | ---------------------------------- | ----------------------------------- |
| Variable  | Data container                       | Local, instance, static, parameter | `int x;`                            |
| Member    | Anything inside a class              | Variables, methods, constructors   | `name`, `display()`                 |
| Field     | Variable belonging to a class/object | Instance or static                 | `String name;`, `static int count;` |
| Attribute | Field representing object’s property | Conceptual / design term           | `name`, `age`                       |

# 3. Methods

* Methods define the behavior (actions) of objects.
```java
class Student {

    String name;
    int age;

    void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}
```
### Calling a Method
```java
public class Main {
    public static void main(String[] args) {

        Student s1 = new Student();

        s1.name = "Alice";
        s1.age = 20;

        s1.display();
    }
}
```
* Methods allow objects to perform actions

* s1.display() calls the method of the object
# 4. Constructor

A constructor initializes object data when the object is created.
```java
class Student {

    String name;
    int age;

    Student(String n, int a) {
        name = n;
        age = a;
    }

    void display() {
        System.out.println(name + " " + age);
    }
}
```
### Main Program
```java
public class Main {
    public static void main(String[] args) {

        Student s1 = new Student("Alice", 20);

        s1.display();
    }
}
```
* Constructors run automatically when an object is created

* They help initialize object attributes

# 5. Access Modifiers

Access modifiers control how class members are accessed.

Example using private:
```java
class Student {

    private String name;
    private int age;

    Student(String n, int a) {
        name = n;
        age = a;
    }

    void display() {
        System.out.println(name + " " + age);
    }
}
```

### Attempting to Access Private Variables
```java
public class Main {
    public static void main(String[] args) {

        Student s1 = new Student("Alice", 20);

        System.out.println(s1.name); // Error: cannot access private variable
        System.out.println(s1.age);  // Error: cannot access private variable
    }
}
```

* private variables cannot be accessed outside the class

* This helps protect object data