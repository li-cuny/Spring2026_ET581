
# For Loop Exercises

---

## 1. Product of Numbers

Calculate the product of numbers from **1 to 5** using a `for` loop.

**Expected Output:**
```
Product = 120
```

---

## 2. Count Letter Occurrences

Ask the user to enter:  
- A word or sentence (as a `String`)  
- A single letter to search for  ( or you can hardcode into your program)

Use a `for` loop to count how many times that letter appears.

**Example:**
```
Input text: programming
Letter to search: g
Output: 2 times
```

---

## 3. Remove Specific Character

Ask the user to enter a word.  
Print the word again **without the letter `'a'`** using a `for` loop.

**Example:**
```
Input: banana
Output: bnn
```

---

## 4. Count Words in a Sentence

Ask the user to enter a sentence.  
Use a `for` loop to count how many words it contains.  
(Assume words are separated by spaces.)

**Example:**
```
Input: Java is fun
Output: 3 words
```

---

## 5. Password Attempts

Correct password: `"java123"`  

Use a `for` loop to allow **3 attempts maximum**:  
- If correct → print `"Access Granted"` and stop using `break`  
- If wrong after 3 tries → print `"Access Denied"`
**Example:**
```
Enter password: hello
Wrong password. Try again.
Enter password: java123
Access Granted
```
```
Enter password: hello
Wrong password. Try again.
Enter password: 123java
Wrong password. Try again.
Enter password: pass
Access Denied
```
---

## 6. Sum Until Condition

Use a `for` loop to add numbers starting from 1 upward.  
Stop the loop using `break` when the **sum becomes greater than 50**.  
Print the final sum.
**Example:**
```
Adding: 5
Adding: 10
Adding: 15
Adding: 20
Sum exceeded 50: 50
```
---

## 7. Print Uppercase Letters

Print all uppercase letters from **A to Z** using a `for` loop.

**Expected Output:**
```
A B C D ... Z
```
**Hint:**  
- Use a `char` variable in the loop and increament by 1.
- Print each character with a space  