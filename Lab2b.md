
## Comparison Operators

| Operator | Description           | Example                   |
|----------|----------------------|---------------------------|
| `==`     | Equal to             | `5 == 5` → true          |
| `!=`     | Not equal to         | `5 != 3` → true          |
| `>`      | Greater than         | `5 > 3` → true           |
| `<`      | Less than            | `5 < 3` → false          |
| `>=`     | Greater than or equal| `5 >= 5` → true          |
| `<=`     | Less than or equal   | `5 <= 6` → true          |

**Compare numbers:**
```java
int a = 10, b = 20;
System.out.println(a < b); // true
```

**Compare Strings:**
```java
String s1 = "Hello";
String s2 = "World";
System.out.println(s1.equals(s2)); // false
```
## Logical Operators

- `&&` : AND  
- `||` : OR  
- `!`  : NOT  

**Example:**
```java
boolean a = true;
boolean b = false;

System.out.println(a && b); // false
System.out.println(a || b); // true
System.out.println(!a);     // false
```
### Short-Circuit Evaluation

Short-circuit evaluation means that in a logical expression, Java may **skip evaluating the second operand** if the result can already be determined from the first operand.


- `&&` (Logical AND)
- `||` (Logical OR)

## Rules

| Operator | Skip Right Operand When | Example |
|----------|------------------------|---------|
| `&&` | Left operand is false | `false && (anything)` → right not evaluated |
| `\|\|` | Left operand is true  | `true \|\| (anything)` → right not evaluated |