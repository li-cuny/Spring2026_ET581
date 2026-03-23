# Nested / Inner Classes

### **Purpose**
Group related classes to improve **readability** and **maintainability**.

### **Accessing Inner Class**
```java
class Outer {
    int x = 10;

    class Inner {
        void show() {
            System.out.println("Outer x = " + x);
        }
    }
}
```
```java
Outer o = new Outer();
Outer.Inner i = o.new Inner();
i.show();  // Outer x = 10
```

---

### **Other Types of Inner Classes**

#### Private Inner Class
- Not accessible from outside the outer class.
```java
class Library {
    private String name;

    // Private inner class
    private class Staff {
        private String staffName;

        Staff(String staffName) {
            this.staffName = staffName;
        }

        void display() {
            System.out.println("Staff Name: " + staffName + ", Library: " + name);
        }
    }

    Library(String name) {
        this.name = name;
    }

    // Method inside outer class can access private inner class
    void showStaff(String staffName) {
        Staff s = new Staff(staffName);
        s.display();
    }
}

public class Main {
    public static void main(String[] args) {
        Library lib = new Library("Central Library");
        lib.showStaff("Alice");  
    }
}
```
#### Static Inner Class
- Can be accessed **without creating** an outer class object.

```java
Outer.StaticInner inner = new Outer.StaticInner();
```

✅ **Advantage:** Inner classes can access outer class **attributes and methods**, even if they are `private`.

* **Note**:A top-level class (not nested inside another class) cannot be static.
    ```java
    static class Parent {  
        // ❌ Compile-time error
    }
    ```
---
# Design Patterns


---

## 1. Singleton Pattern

**Purpose:** Ensure only **one instance** of a class exists.  
**Use case:** Logger, configuration, database connection.

```java
class Logger {
    private static Logger instance;

    private Logger() {}

    public static Logger getInstance() {
        if (instance == null) {
            instance = new Logger();
        }
        return instance;
    }

    public void log(String message) {
        System.out.println("LOG: " + message);
    }
}

public class Main {
    public static void main(String[] args) {
        Logger log1 = Logger.getInstance();
        Logger log2 = Logger.getInstance();
        log1.log("Hello World!");
        System.out.println(log1 == log2); // true
    }
}
```
## 2. Builder Pattern

- Purpose: Build complex objects step by step, especially with optional fields.
```java
class User {
    private String name;
    private int age;
    private String email;

    static class Builder {
        private String name;
        private int age;
        private String email;

        Builder setName(String name) { this.name = name; return this; }
        Builder setAge(int age) { this.age = age; return this; }
        Builder setEmail(String email) { this.email = email; return this; }

        User build() {
            User u = new User();
            u.name = this.name;
            u.age = this.age;
            u.email = this.email;
            return u;
        }
    }

    void display() {
        System.out.println(name + ", " + age + ", " + email);
    }
}

public class Main {
    public static void main(String[] args) {
        User user = new User.Builder()
                        .setName("Alice")
                        .setAge(25)
                        .setEmail("alice@example.com")
                        .build();
        user.display();
    }
}
```