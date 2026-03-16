# Java OOP Exercise Questions – Student & Car Examples

This file contains exercises to practice **Encapsulation, `this` keyword, object fields, object as method parameter, static members, and composition** in Java.

---

## 1. Getters and Setters (Encapsulation)

1. Create a `Student` class with private fields: `name` (String) and `marks` (int).  
   - Add getters and setters for both fields.  
   - In `main`, create a student object, update the marks using the setter, and print all details using getters.

2. Modify the setter for `marks` to **prevent negative values**. Test your program with a negative input.  

3. Create an `Employee` class with `name` and `salary`.  
   - Add getters and setters.  
   - Add a method `giveRaise(double percent)` that increases the salary using the setter.  

---

## 2. `this` Keyword

4. Create a `Rectangle` class with fields `length` and `width`.  
   - Use `this` in the constructor to differentiate parameters from fields.  
   - Add methods to calculate area and perimeter.

5. Create a `Person` class that prints a greeting in the constructor: `"Hello, my name is <name>"` using `this`.  

---

## 3. Object as Field (Composition / Aggregation)

6. Create a class `Address` with fields `city` and `country`.  
   - Create a `Student` class with `name`, `age`, and an `Address` object as a field.  
   - Write a method `display()` that prints student details including the address.

7. Modify the above so that the `Address` object is **created outside** the `Student` constructor and passed in (aggregation).  

8. Create a `Car` class with a field `Engine` engine (fields: `type`, `horsepower`).  
   - Use composition engine field to display the car and engine details.  

9. Challenge: Modify the `Car` class to have **two Engine objects** (e.g., hybrid car) and display both engines.  

---

## 4. Object as Method Parameter

10. Modify the `Student` class to include a method `greet(Student other)` that prints:  
    `"Hello <other.name>, I am <this.name>!"`.  
    - Create two student objects and call `greet()` both ways.  

11. Add a method `isSameStudent(Student other)` that returns `true` if both students have the same `name` and `marks`.  

12. Create a method `swapMarks(Student other)` that swaps the marks between two students.  

---

## 5. Static Members

13. Add a static field `count` to the `Student` class that tracks how many student objects have been created.  
    - Add a static method `showCount()` to display the total number of students.  

14. Create a `School` class with a static field `schoolName`.  
    - Change the school name using one student object and demonstrate that it affects all students.  

---

## 6. Optional Challenge – Combining Concepts

**Exercise:**  

Create a small **Library system** using **arrays** . The system should have the following:

1. **Classes**:  
   - `Library`  
   - `Book`  
   - `Author`  

2. **Class Details**:  
   - `Library` has an **array of `Book` objects** (e.g., size 10) and a variable to keep track of the number of books added.  
   - `Book` has fields: `title` (String) and `Author` object.  
   - `Author` has fields: `name` and any other detail you like.  

3. **Requirements**:  
   - Add **getters and setters** for all fields.  
   - Add a **static field** in `Book` to track the total number of books created.  
   - Add methods in `Library` to:  
     - Add a `Book` to the array.  
     - Display all books with their author details.  

4. **Demonstration**:  
   - In `main`, create a few `Author` objects.  
   - Create several `Book` objects using those authors.  
   - Add them to the `Library` array.  
   - Display all books and show the **total number of books** using the static field.  

**Hints:**  
- Use a fixed-size array, e.g., `Book[] books = new Book[10];`  
- Keep track of how many books are currently in the array with a `count` variable.  
- Use a loop to display all the books.  

