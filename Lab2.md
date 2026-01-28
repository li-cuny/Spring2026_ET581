# Classes and Objects Terminology

## Class

A class definition is a **blueprint**  for creating objects.
```
class Car {
    // class body

}
```

### Object
An object is a specific instance of a class.
* It stores data (in fields) and can perform actions (via methods) as defined by its class.

```
Car car = new Car(); // create a Car object

```
### Method

A method is a block of code that performs a specific task.

* A method can take parameters, perform operations, and return a value (or return nothing).value**.
```java
//syntax
returnType methodName(parameters) {
    // method body
    // statements to perform the action
    return value; // if returnType is not void
}
// example
int getNextNumber(int n){
    n = n + 1;
    return n;
}
```
* Invoking (Calling) a Method
 `objectName.methodName()`
* Example:

```java
car.start(); // car is calling object
Car.countNumberOfCars();
```


## String Class
- String is a predefined class in Java.

- Objects of type String store a sequence of characters.

- Strings are written inside double quotes (" ").
```java
String motto = "String is sequence of chars.";
```
### String methods

## 1.. `length()`
**Definition:**
```java
int length()
```
- Returns the number of characters in the string.

**Example:**
```java
String text = "Programming";
int len = text.length();  // len = 11
len = "Hi".length(); 
```
## 2. `equals()`
**Definition:**
```java
boolean equals(String other)
```
- Compares the content of the calling string with another string.

**Example:**
```java
String greeting = "Hello";
greeting.equals("Hello")//true 
```

## 3. `charAt()`
**Definition:**
```java
char charAt(int index);
```
- Returns the character at a specific index (starting at 0).

**Example:**
```java
String word = "Java";
char ch = word.charAt(2);  // ch = 'v'
```


**Full method list:** [Java String API](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)
