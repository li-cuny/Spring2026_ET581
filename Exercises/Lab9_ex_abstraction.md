# Lab 9 — Exercises (Abstract Classes & Interfaces)

---

### Exercise 1: Animal Behavior System
Topic: Abstract class + method overriding

You are designing a simple animal simulation system.

Create an abstract class `Animal` with:
- A method `sound()` (abstract)
- A method `sleep()` that prints: "Sleeping..."

Create a class `Dog` that:
- Extends `Animal`
- Implements `sound()` to print: "Dog barks"

Goal: Understand how abstract methods force subclasses to define behavior.

---

### Exercise 2: Multiple Animal Types
Topic: Inheritance with abstract class

Extend the previous `Animal` class.

Create two subclasses:
- `Dog` → prints "Dog barks"
- `Cat` → prints "Cat meows"

In main method:
- Create references of type `Animal`
- Assign `Dog` and `Cat` objects and call `sound()`

Goal: Understand runtime polymorphism with abstract classes.

---

### Exercise 3: Shape Area System
Topic: Template design using abstraction

Design a shape calculation system.

Create an abstract class `Shape`:
- abstract method `area()`
- method `info()` → prints "This is a shape"

Create:
- `Circle` (use radius)
- `Rectangle` (use length and width)

In main method:
- Store different shapes in `Shape` reference
- Call `area()` for each object

Goal: Understand shared structure with different implementations.

---

### Exercise 4: Vehicle Initialization System
Topic: Abstract class with constructor

Create an abstract class `Vehicle`:
- Field: `brand`
- Constructor to initialize brand
- Abstract method `start()`

Create subclasses:
- `Car`
- `Bike`

Each subclass should:
- Print its brand in `start()` method

Goal: Understand constructors in abstract classes.

---

### Exercise 5: Drawing System
Topic: Interface implementation

Create an interface `Drawable`:
- Method `draw()`

Create classes:
- `Circle`
- `Square`
- `Triangle`

Each class should implement `draw()` differently.

In main method:
- Use `Drawable` reference to call methods

Goal: Understand contract-based design.

---

### Exercise 6: Media Player System
Topic: Multiple implementations of same interface

Create an interface `Playable`:
- Method `play()`

Create classes:
- `Guitar`
- `Piano`

Each should implement `play()` with different output.

Goal: Understand same interface, different behavior.

---

### Exercise 7: Flying and Swimming Behavior
Topic: Multiple inheritance using interfaces

Create two interfaces:
- `Flyable` → method `fly()`
- `Swimmable` → method `swim()`

Create class `Duck`:
- Implements both interfaces
- Defines both behaviors

In main method:
- Call both `fly()` and `swim()`

Goal: Understand multiple interfaces in a single class.

---

### Exercise 8: Vehicle System with Default Behavior
Topic: Default methods

Create interface `Vehicle`:
- Abstract method `run()`
- Default method `start()` → prints "Vehicle is starting"

Create classes:
- `Car`
- `Bus`

Each class:
- Implements `run()`
- Uses or overrides `start()`

Goal: Understand reusable behavior in interfaces.

---

### Exercise 9: Payment Processing System
Topic: Interface + polymorphism

Design a payment system.

Create interface `Payment`:
- Method `pay(double amount)`

Create classes:
- `CreditCardPayment`
- `UPIPayment`
- `CashPayment`

In main method:
- Create `Payment` reference
- Assign different payment types dynamically
- Call `pay()` with different amounts

Goal: Understand runtime polymorphism using interfaces.

---

### Exercise 10: Employee Management System
Topic: Abstract class + interface combined

Design an employee system.

Create abstract class `Employee`:
- Field: `name`
- Constructor to initialize name
- Abstract method `calculateSalary()`

Create interface `BonusEligible`:
- Method `bonus()`

Create class `Manager`:
- Extends `Employee`
- Implements `BonusEligible`
- Salary = fixed + bonus

In main method:
- Create `Manager` object
- Call both salary calculation and bonus methods

Goal: Combine abstraction and interfaces in a real-world design.