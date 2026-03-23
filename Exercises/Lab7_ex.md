# Singleton Exercise: TheSun ☀️
---

## Instructions

1. Create a class `TheSun`.
2. Make the constructor **private** to prevent multiple instances.
3. Add a **static method** `getInstance()` that returns the single instance of `TheSun`.
4. Add a method `shine()` that prints:
```
The sun is shining!
```
5. In the `main` method:
- Get **two references** to `TheSun`.
- Call `shine()` using both references.
- Verify that both references point to the **same instance** using `==`.

---

## Optional Challenge
- Add a field `brightness` to `TheSun`.
- Set it only **once** inside the Singleton.
- Print the brightness value inside the `shine()` method.

---

## Sample Output
```
The sun is shining!
The sun is shining!
true
```

> The last line `true` indicates that both references point to the **same instance**.

# Builder Pattern Exercise: Spaceship 🚀


## Instructions

1. Create a class `Spaceship` with the following **fields**:
   - `name` (String)
   - `fuelType` (String)
   - `crewCapacity` (int)
   - `speed` (double)
   - `hasShield` (boolean)

2. Inside `Spaceship`, create a **static inner class** called `Builder`.

3. Builder class should have **setter methods** for each field:
   - Each setter should **return `this`** so calls can be chained.

4. Builder class should have a **`build()`** method that:
   - Creates a new `Spaceship` object.
   - Sets all fields from the Builder.
   - Returns the new `Spaceship`.

5. In the `Spaceship` class, add a method `displaySpecs()` that prints all the fields.

6. In `main`:
   - Use the Builder to create a `Spaceship` with **all fields set**.
   - Use the Builder to create a `Spaceship` with only `name` and `crewCapacity` set.
   - Call `displaySpecs()` for each spaceship.

---

## Optional Challenge
- Make `speed` default to `0` if not set.
- Make `hasShield` default to `false` if not set.

---

## Sample Output
```
Spaceship Name: Star Voyager
Fuel Type: Ion
Crew Capacity: 5
Speed: 9000.5
Has Shield: true

Spaceship Name: Explorer
Fuel Type: null
Crew Capacity: 2
Speed: 0.0
Has Shield: false
```

> Notice that fields not set in the Builder remain default (`null`, `0`, or `false`).