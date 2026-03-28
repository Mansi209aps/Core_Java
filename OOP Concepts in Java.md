# 🔥 3. OOP Concepts in Java

OOP = **Object-Oriented Programming**

👉 It is a programming paradigm based on **objects and classes**.

---

# 📌 Core Pillars of OOP

1. Encapsulation
2. Abstraction
3. Inheritance
4. Polymorphism

---

# 1️⃣ Encapsulation

### 👉 Definition

Encapsulation means **wrapping data (variables) and methods into a single unit (class)** and **restricting direct access**.

---

### 🔹 How to achieve:

* Make variables **private**
* Provide **getter & setter methods**

---

### Example:

```java
class Student {
    private int marks;

    public int getMarks() {
        return marks;
    }

    public void setMarks(int marks) {
        this.marks = marks;
    }
}
```

---

### 🔹 Benefits:

* Data hiding
* Security
* Controlled access

---

### 🔹 Interview Trap:

👉 Encapsulation ≠ just data hiding
👉 It is **binding data + methods together**

---

# 2️⃣ Abstraction

### 👉 Definition

Abstraction means **hiding implementation details and showing only essential features**.

---

### 🔹 Ways to achieve:

1. Abstract class
2. Interface

---

### Example (Abstract Class):

```java
abstract class Vehicle {
    abstract void start();
}
```

---

### 🔹 Key Points:

* Cannot create object of abstract class
* Can have:

  * Abstract methods (no body)
  * Concrete methods (with body)

---

### 🔹 Real-life Example:

👉 ATM → You use it without knowing internal logic

---

# 3️⃣ Inheritance

### 👉 Definition

Inheritance allows one class to **acquire properties of another class**.

---

### 🔹 Syntax:

```java
class Child extends Parent {
}
```

---

### 🔹 Types of Inheritance in Java

| Type         | Supported       |
| ------------ | --------------- |
| Single       | ✅               |
| Multilevel   | ✅               |
| Hierarchical | ✅               |
| Multiple     | ❌ (via classes) |
| Hybrid       | ❌               |

👉 Multiple inheritance is achieved using **interfaces**

---

### 🔹 Example:

```java
class Animal {
    void eat() {
        System.out.println("Eating");
    }
}

class Dog extends Animal {
}
```

---

### 🔹 Keywords:

* `extends`
* `super`

---

### 🔹 super keyword uses:

* Call parent constructor
* Access parent method/variable

---

# 4️⃣ Polymorphism

### 👉 Definition

Polymorphism means **one name, many forms**.

---

## 🔹 Types:

---

### 1. Compile-time Polymorphism (Method Overloading)

```java
class MathUtil {
    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }
}
```

---

### Rules:

* Same method name
* Different parameters

---

---

### 2. Runtime Polymorphism (Method Overriding)

```java
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Bark");
    }
}
```

---

### 🔹 Achieved using:

* Inheritance
* Method overriding

---

### 🔹 Important Rules:

* Method signature must be same
* Cannot reduce access level
* Final methods cannot be overridden

---

---

# 📌 Important Supporting Concepts

---

## 🔹 1. Class

Blueprint of object

```java
class Car {
}
```

---

## 🔹 2. Object

Instance of class

```java
Car c = new Car();
```

---

## 🔹 3. Constructor

Special method used to initialize objects

---

### Types:

* Default constructor
* Parameterized constructor

---

### Example:

```java
class Car {
    Car() {
        System.out.println("Car created");
    }
}
```

---

## 🔹 4. this keyword

Refers to current object

---

### Uses:

* Resolve variable conflict
* Call constructor

```java
this.name = name;
```

---

## 🔹 5. super keyword

Refers to parent class

---

## 🔹 6. Method Overloading vs Overriding

| Feature     | Overloading  | Overriding |
| ----------- | ------------ | ---------- |
| Time        | Compile-time | Runtime    |
| Inheritance | Not required | Required   |
| Parameters  | Different    | Same       |

---

# ⚠️ Important Interview Edge Cases

---

### ❗ Can we override static methods?

👉 No (method hiding happens)

---

### ❗ Can we override private methods?

👉 No

---

### ❗ Can constructors be inherited?

👉 No

---

### ❗ Can abstract class have constructor?

👉 Yes

---

### ❗ Can we create object of abstract class?

👉 No

---

### ❗ Can interface have variables?

👉 Yes → by default:

* `public static final`

---

# 🎯 Real-Life Example (Best for Interviews)

👉 Example: **Car System**

* Encapsulation → speed hidden inside class
* Abstraction → user only sees drive()
* Inheritance → ElectricCar extends Car
* Polymorphism → different cars behave differently

---

# 🧠 Memory Trick

👉 **E A I P**

* Encapsulation
* Abstraction
* Inheritance
* Polymorphism

---

# 🎯 Interview Summary Answer

If asked:

> “Explain OOP concepts”

You say:

> OOP in Java is based on four pillars: Encapsulation (data hiding), Abstraction (hiding implementation), Inheritance (code reuse), and Polymorphism (multiple behavior using same method).

---

# ⚡ Pro Tip (VERY IMPORTANT FOR YOU)

Interviewers don’t just want definitions. They will ask:

* Real-life examples
* Differences
* Code snippets
* Edge cases

👉 Always combine:
**Definition + Example + Rule**

---
