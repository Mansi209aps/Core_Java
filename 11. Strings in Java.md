# 🔷 1. What is String in Java?

* A **String** is an **immutable object** representing a sequence of characters.
* Class: `String` (in `java.lang`)
* Internally uses **char[] (before Java 9)** or **byte[] (Java 9+)**

---

# 🔷 2. Memory Management (VERY IMPORTANT 🔥)

## ➤ String Constant Pool (SCP)

* Special memory area inside Heap
* Stores **unique string literals**

```java
String s1 = "Java";
String s2 = "Java";
```

👉 Both refer to **same object in SCP**

---

## ➤ Heap Memory

```java
String s3 = new String("Java");
```

👉 Creates:

* 1 object in Heap
* 1 in SCP (if not already present)

---

## ➤ Interview Insight

* `"Java"` → SCP
* `new String("Java")` → Heap + SCP

---

# 🔷 3. Immutability (MOST ASKED ⭐)

## ➤ Why Strings are Immutable?

* Security (used in class loading, URLs, etc.)
* Thread-safe
* Enables **String Pool optimization**

```java
String s = "Hello";
s.concat(" World");
```

👉 Output: `"Hello"` (unchanged)

---

## ➤ How it works internally?

* Instead of modifying, Java creates **new object**

---

# 🔷 4. String Comparison

## ➤ `==` (Reference Comparison)

```java
s1 == s2
```

* Checks memory location

## ➤ `equals()` (Content Comparison)

```java
s1.equals(s2)
```

* Checks actual value

👉 Interview trap:

```java
String a = new String("Java");
String b = new String("Java");

a == b       // false
a.equals(b)  // true
```

---

# 🔷 5. Important Methods (High Frequency)

| Method        | Purpose          |
| ------------- | ---------------- |
| `length()`    | Length of string |
| `charAt()`    | Character access |
| `substring()` | Extract part     |
| `contains()`  | Check substring  |
| `replace()`   | Replace chars    |
| `split()`     | Split string     |
| `trim()`      | Remove spaces    |

---

# 🔷 6. String vs StringBuilder vs StringBuffer

| Feature     | String                    | StringBuilder | StringBuffer        |
| ----------- | ------------------------- | ------------- | ------------------- |
| Mutability  | Immutable                 | Mutable       | Mutable             |
| Thread-safe | Yes                       | No            | Yes                 |
| Performance | Slow (due to new objects) | Fast          | Slower than Builder |

👉 Interview answer:

* Use **StringBuilder** for performance
* Use **StringBuffer** in multithreading

---

# 🔷 7. String Interning

```java
String s1 = new String("Java");
String s2 = s1.intern();
```

👉 `intern()` → moves string to SCP

---

# 🔷 8. String Concatenation

## ➤ Using `+`

```java
String s = "Java" + "World";
```

## ➤ Using `concat()`

```java
s.concat("World");
```

👉 Behind the scenes:

* Uses **StringBuilder** for optimization (compiler level)

---

# 🔷 9. Important Interview Scenarios

## ➤ Case 1

```java
String s1 = "Java";
String s2 = "Ja" + "va";
```

👉 `s1 == s2` → **true** (compile-time optimization)

---

## ➤ Case 2

```java
String s1 = "Java";
String s2 = new String("Java");
```

👉 `s1 == s2` → **false**

---

## ➤ Case 3

```java
String s1 = "Java";
String s2 = s1.concat("World");
```

👉 New object created

---

# 🔷 10. Conversion (Frequently Asked)

* String → int

```java
Integer.parseInt("123");
```

* int → String

```java
String.valueOf(123);
```

---

# 🔷 11. Why String is Final Class?

* Prevents modification
* Ensures immutability
* Improves security

---

# 🔷 12. Best Practices (Interview Ready Answers ✅)

* Always use **`equals()` instead of `==`**
* Prefer **StringBuilder** for multiple modifications
* Avoid unnecessary `new String()`
* Use **String Pool efficiently**

---

# 🔷 13. One-Line Summary (Perfect Interview Ending 🎯)

👉 *"String in Java is an immutable, pooled object optimized for performance, security, and memory efficiency."*

---
