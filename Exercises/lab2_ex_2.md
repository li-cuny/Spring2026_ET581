# Java Exercises – Conditional Statements & StringTokenizer

## 1. if / else Exercises

### Exercise 1
Write a Java program that checks whether a number is **divisible by 5**.

**Expected Output**
- "Divisible by 5"
- "Not divisible by 5"

---

### Exercise 2
Given two String `a` and `b`, write a program that prints:
- "Equal" if both Strings are the same  
- "Not Equal" otherwise

---

## 2. Ternary Operator Exercises

### Exercise 3
Using a **ternary operator**, assign:
- "Maximum" if `a > b`
- "Minimum" otherwise

---

### Exercise 4
Given an integer `temp`, store the result in a variable:
- "Hot" if temperature ≥ 30  
- "Normal" otherwise  

Use **only the ternary operator**.

---

## 3. switch Exercises

### Exercise 5
Write a program using `switch` that:
- Takes a character (`A`, `E`, `I`, `O`, `U`)
- Prints "Vowel" if it is a vowel
- Prints "Consonant" for any other character

---

### Exercise 6
Predict the output of the following code and explain why:

```java
int choice = 3;

switch (choice) {
    case 1:
        System.out.print("One ");
        break;
    case 2:
        System.out.print("Two ");
    case 3:
        System.out.print("Three ");
        break;
    default:
        System.out.print("Default ");
}
```
## 4. StringTokenizer Exercises
### Exercise 7
Given the following string:
```java
String text = "red|green|blue|yellow";
```
Use StringTokenizer to print each color on a new line.

### Exercise 8
Given:
```java
String numbers = "5:10:15";
```
* Use StringTokenizer

* Calculate and print the average of the numbers

## 5. Challenge Exercise
### Exercise 9
Given:
```java
String input = "A,B,,C,D,,";
```
Tasks:

* Use StringTokenizer

* Count how many non-empty tokens are present

* Print the count