# Lab7 Inheritance Practice Exercises

---

## Section 1: Parent and Child Class with Fields

### Exercise 1: Animal System
**Parent Class:** Animal  
**Child Class:** Dog  

**Fields:**
- Animal (Parent): name, age
- Dog (Child): breed

**Task:**
Create a Dog object and print all fields.

---

### Exercise 2: Person System
**Parent Class:** Person  
**Child Class:** Student  

**Fields:**
- Person (Parent): name, age
- Student (Child): schoolName

**Task:**
Print all details using Student object.

---

### Exercise 3: Vehicle System
**Parent Class:** Vehicle  
**Child Class:** Bike  

**Fields:**
- Vehicle (Parent): brand, speed
- Bike (Child): hasGear (boolean)

**Task:**
Create Bike object and display all values.

---

## Section 2: Constructors and super keyword

### Exercise 4: Animal Constructor
**Parent Class:** Animal  
**Child Class:** Dog  

**Fields:**
- Animal (Parent): name
- Dog (Child): breed

**Constructors:**
- Animal(String name)
- Dog(String name, String breed)

**Task:**
Use super(name) and print both fields.

---

### Exercise 5: Student Constructor
**Parent Class:** Person  
**Child Class:** Student  

**Fields:**
- Person (Parent): name
- Student (Child): schoolName

**Constructors:**
- Person(String name)
- Student(String name, String schoolName)

**Task:**
Use super(name) in Student.

---

### Exercise 6: Vehicle Constructor Flow
**Parent Class:** Vehicle  
**Child Class:** Bike  

**Fields:**
- Vehicle (Parent): brand
- Bike (Child): type

**Task:**
Observe constructor calling order when creating Bike object.

---

## Section 3: Method Overriding

### Exercise 7: Animal Sound System
**Parent Class:** Animal  
**Child Class:** Dog  

**Fields:**
- Animal (Parent): name

**Methods:**
- sound()

Dog overrides sound()

**Task:**
Create Animal reference pointing to Dog object and call sound().

---

### Exercise 8: Vehicle Movement
**Parent Class:** Vehicle  
**Child Class:** Bike  

**Fields:**
- Vehicle (Parent): speed

**Methods:**
- move()

Bike overrides move()

**Task:**
Call move() using Bike object.

---

### Exercise 9: Person Work System
**Parent Class:** Person  
**Child Class:** Student  

**Fields:**
- Person (Parent): name

**Methods:**
- work()

Student overrides work()

**Task:**
Create Student object and call work().

---

## Section 4: Method Overloading

### Exercise 10: Calculator
**Class (No Inheritance)**
- Calculator

**Fields:**
- name

**Methods:**
- add(int a, int b)
- add(int a, int b, int c)

**Task:**
Call all overloaded methods.

---

### Exercise 11: Display System
**Class (No Inheritance)**
- Display

**Methods:**
- display(String name)
- display(int age)

**Task:**
Call both methods.

---

## Section 5: Two-Level Inheritance

### Exercise 12: Animal Chain
**Parent Class:** Animal  
**Child Class:** Dog  
**Grandchild Class:** Puppy  

**Fields:**
- Animal (Parent): name
- Dog (Child): breed
- Puppy (Grandchild): size

**Task:**
Create Puppy object and print all fields.

---

### Exercise 13: Vehicle Chain
**Parent Class:** Vehicle  
**Child Class:** Car  
**Grandchild Class:** ElectricCar  

**Fields:**
- Vehicle (Parent): brand
- Car (Child): model
- ElectricCar (Grandchild): batteryCapacity

**Task:**
Access all fields using ElectricCar object.

---

