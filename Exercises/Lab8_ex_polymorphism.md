# Lab8
---

## 1. Shape Array (Polymorphism - Area Calculation)

### 🔧 Question  
Create a Shape hierarchy using polymorphism and store objects in an array. Then find the shape with the maximum area.

---

### 🧱 Classes  
- `Shape` → `area()`  
- `Circle` → overrides `area()` (πr²)  
- `Rectangle` → overrides `area()` (l × w)  
- `Triangle` → overrides `area()` (½ × b × h)  

---

### 📦 Task  
```java
Shape[] shapes = new Shape[5];
```
Fill the array with different shape objects.

### 🎯 Requirements
- Loop through the array and call area() for each shape
- Print the area of each shape
- Find and print the shape with the maximum area
- Demonstrate runtime polymorphism using Shape reference

## 2. Employee Salary System 

### 🔧 Question  
Design an Employee Salary System using **runtime polymorphism**. Store different types of employees in an array and calculate their salaries based on their roles.

---

### 🧱 Classes  

#### 1. `Employee` (Parent Class)
- Fields:
  - `String name`
  - `double baseSalary`
- Method:
  - `double calculateSalary()`

---

#### 2. `Developer` (Child Class)
- Field:
  - `double bonus`
- Overrides:
  - `calculateSalary() = baseSalary + bonus`

---

#### 3. `Designer` (Child Class)
- Field:
  - `double commission`
- Overrides:
  - `calculateSalary() = baseSalary + commission`

---

#### 4. `Manager` (Child Class)
- Field:
  - `double allowance`
- Overrides:
  - `calculateSalary() = baseSalary + allowance`

---

### 📦 Task  
Create an array of employees:
```java
Employee[] employees = new Employee[5];
```
### 🎯 Requirements
- Store different employee objects in array
- Loop through array and call calculateSalary()
- Print salary of each employee
- Calculate and print total salary of company
