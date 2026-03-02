

## Math Class in Java
| Method   | Description             |
| -------- | ----------------------- |
| max(a,b) | Returns larger value    |
| min(a,b) | Returns smaller value   |
| abs(x)   | Absolute value          |
| sqrt(x)  | Square root             |
| pow(a,b) | Power                   |
| random() | Random number [0.0–1.0) |
| round(x) | Rounds number           |
| ceil(x)  | Rounds up               |
| floor(x) | Rounds down             |

Math class java doc: https://docs.oracle.com/javase/8/docs/api/?java/lang/Math.html
 
- `(int)(Math.random() * 101)` → random number [0,100]  

---
## Generating Random Numbers

### Using `Math.random()`
```java
double r = Math.random();
int n = (int)(Math.random() * 10); // 0 to 9
```

### Using `Random` Class
```java
import java.util.Random;

Random rand = new Random();

// Random double 0.0 <= x < 1.0
double rDouble = rand.nextDouble();

// Random int between 0 and 9
int rInt = rand.nextInt(10);

// Random boolean
boolean rBool = rand.nextBoolean();
```
- More versatile than `Math.random()`.
- Can set a **seed** for reproducible results.

---

### Method Overloading
- Same method name, different parameter list.
```java
int square(int x);
double square(double x);
```

