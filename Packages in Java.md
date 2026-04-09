# 🔥 Packages in Java

## 📌 1. Definition

A **package** is a **namespace that groups related classes and interfaces**.

👉 Purpose:

* Organize code
* Avoid name conflicts
* Provide access control

# 📌 2. Types of Packages

## 🔹 1. Built-in Packages

Provided by Java API

👉 Examples:

* `java.lang` (default package)
* `java.util`
* `java.io`

---

## 🔹 2. User-defined Packages

Created by developer

```java id="d2z2o8"
package com.myapp;
```

# 📌 3. Creating a Package

## 📌 Syntax

```java id="caxh64"
package packageName;
```

## 📌 Example

```java id="9u5r86"
package com.demo;

public class Test {
    public void show() {
        System.out.println("Hello");
    }
}
```


## 💡 Explanation

* Package declared at top
* Class belongs to `com.demo` package

# 📌 4. Compiling & Running

```bash id="ty4sq5"
javac -d . Test.java
java com.demo.Test
```

👉 `-d` creates folder structure

# 📌 5. Accessing Packages (import)


## 🔹 1. Import specific class

```java id="3n7m43"
import java.util.ArrayList;
```

## 🔹 2. Import entire package

```java id="aq8xqo"
import java.util.*;
```

# 📌 6. Default Package

👉 If no package is declared:

* Class belongs to **default package**
* Not recommended for large projects

# 📌 7. Access Control in Packages

| Modifier  | Same Class | Same Package | Subclass | Other Package |
| --------- | ---------- | ------------ | -------- | ------------- |
| private   | ✅          | ❌            | ❌        | ❌             |
| default   | ✅          | ✅            | ❌        | ❌             |
| protected | ✅          | ✅            | ✅        | ❌*            |
| public    | ✅          | ✅            | ✅        | ✅             |

👉 *protected works outside package via inheritance

# 📌 8. Subpackages

```java id="3r0x8t"
package com.company.project;
```

👉 Creates folder structure:

```text id="4d9w7m"
com/company/project
```

# 📌 9. Naming Convention

* Use **lowercase letters**
* Use **reverse domain name**

👉 Example:

```text id="q0zjap"
com.google.util
com.mycompany.app
```

# 📌 10. Advantages

* Better organization
* Avoid class name conflicts
* Improves reusability
* Provides access protection

# 📌 11. Common Interview Traps

### ❗ `java.lang` is imported by default

### ❗ Cannot import default package into other packages

### ❗ Package statement must be first line


# 📌 12. Static Import (Advanced)

```java id="4u6m6j"
import static java.lang.Math.*;
```

👉 Allows:

```java id="0bqf70"
sqrt(16);
```

instead of:

```java id="7n8nx0"
Math.sqrt(16);
```


# 📌 13. Real-Life Example

👉 Example: Folder structure

* Package = folder
* Classes = files inside folder

---

# 🎯 Interview Summary

> Packages in Java are used to group related classes and interfaces into a namespace, helping in organizing code, avoiding naming conflicts, and controlling access. They can be built-in or user-defined and support hierarchical structuring through subpackages.

---
