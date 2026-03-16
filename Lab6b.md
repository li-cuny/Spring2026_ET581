## 6. Getters and Setters (Encapsulation)

* **Getter**: A method that returns the value of a private field.

* **Setter**: A method that sets or updates the value of a private field.

They are used to encapsulate data, allowing controlled access to `private fields` from `other` classes.


```java
class Student {
    private String name;
    private int age;

    // Constructor
    Student(String n, int a) {
        name = n;
        age = a;
    }

    // Getter for name
    public String getName() {
        return name;
    }

    // Setter for name
    public void setName(String n) {
        name = n;
    }

    // Getter for age
    public int getAge() {
        return age;
    }

    // Setter for age
    public void setAge(int a) {
        age = a;
    }
}
```
* Using Getters and Setters
```java
public class Main {
    public static void main(String[] args) {
        Student s1 = new Student("Alice", 20);

        System.out.println(s1.getName());
        s1.setAge(21);
        System.out.println(s1.getAge());
    }
}
```
* Encapsulation is the principle of hiding data and providing controlled access.
## 7. this Keyword

The `this` keyword in Java is a reference variable that refers to the current object — the object whose method or constructor is being executed.
static method can be called without creating an object, there is no `“current object”` for `this` to refer to.

```java
class Student {
    private String name;
    private int age;

    Student(String name, int age) {
        this.name = name; // 'this' refers to object's field
        this.age = age;
    }
}
```
## 8. Object in field or param
- A field of a class can itself be an object of another class.
```java
class Address {
    String city;
    String country;

    Address(String city, String country) {
        this.city = city;
        this.country = country;
    }

    void displayAddress() {
        System.out.println(city + ", " + country);
    }
}

class Student {
    String name;
    int age;
    Address address; // field is another class object

    Student(String name, int age, Address address) {
        this.name = name;
        this.age = age;
        this.address = address;
    }

    void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.print("Address: ");
        address.displayAddress(); // calling method of field object
    }
}

public class Main {
    public static void main(String[] args) {
        Address a1 = new Address("New York", "USA");
        Student s1 = new Student("Alice", 20, a1);

        s1.display();
    }
}
```
| Feature           | Composition                   | Aggregation                      |
| ----------------- | ----------------------------- | -------------------------------- |
| Ownership         | Strong – parent owns child    | Weak – parent references child   |
| Lifecycle         | Child dies with parent        | Child exists independently       |
| Object Creation   | Created inside parent         | Created outside and passed in    |
| Sharing           | Each parent has its own child | Multiple parents can share child |
| Relationship Type | Part-of                       | Uses-a / Has-a                   |
| Example           | Student → Address             | Student → Department             |

- object in method parameter
```java
class Student {
    private String name;
    // Constructor
    public Student(String name) {
        this.name = name;
    }
    // Method that greets another Student
    public void greet(Student other) {
        System.out.println("Hello " + other.name + ", I am " + this.name + "!");
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student("Alice");
        Student s2 = new Student("Bob");

        s1.greet(s2); // Output: Hello Bob, I am Alice!
        s2.greet(s1); // Output: Hello Alice, I am Bob!
    }
}
```
### 9. Static Members

* The `static` keyword belongs to the class, not to instances (objects).

* Static members (variables or methods) are shared among all objects of the class.

* You can access static members without creating an object.

```java
class Student {
    private String name;
    private int age;
    static int count = 0; // shared by all objects

    Student(String n, int a) {
        name = n;
        age = a;
        count++;
    }

    static void showCount() {
        System.out.println("Total Students: " + count);
    }
}
```