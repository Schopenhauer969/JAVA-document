# ☕ Java — Complete Guide (Beginner to Advanced)

> A complete, hands-on guide to Java — from your first program to OOP, collections, generics, streams, and multithreading used in real production code.

---

## 📚 Table of Contents

1. [Introduction](#1-introduction)
2. [Prerequisites & Setup](#2-prerequisites--setup)
3. [Your First Program](#3-your-first-program)
4. [Variables & Data Types](#4-variables--data-types)
5. [Operators](#5-operators)
6. [Control Flow](#6-control-flow)
7. [Arrays](#7-arrays)
8. [Methods](#8-methods)
9. [OOP: Classes & Objects](#9-oop-classes--objects)
10. [Inheritance & Polymorphism](#10-inheritance--polymorphism)
11. [Interfaces & Abstract Classes](#11-interfaces--abstract-classes)
12. [Exception Handling](#12-exception-handling)
13. [Collections Framework](#13-collections-framework)
14. [Generics](#14-generics)
15. [Streams & Lambda Expressions](#15-streams--lambda-expressions)
16. [File I/O](#16-file-io)
17. [Multithreading Basics](#17-multithreading-basics)
18. [Best Practices](#18-best-practices)
19. [Full Example Project](#19-full-example-project)
20. [Resources](#20-resources)

---

## 1. Introduction

Java is a class-based, object-oriented, statically-typed programming language designed to run anywhere via the **JVM (Java Virtual Machine)** — "write once, run anywhere."

**Key facts:**
- Compiled to bytecode, then run by the JVM (platform-independent)
- Statically typed — variable types are checked at compile time
- Strong OOP foundations: classes, inheritance, interfaces, polymorphism
- Powers Android apps, enterprise backends, big data systems (Hadoop, Spark), and more

---

## 2. Prerequisites & Setup

- No prior coding experience required
- **JDK (Java Development Kit)** 17 or later installed
- A code editor: **IntelliJ IDEA**, **VS Code**, or **Eclipse**

```bash
# Verify installation
java --version
javac --version
```

Expected output (example):
```
java 21.0.1 2023-10-17 LTS
javac 21.0.1
```

**Compiling and running Java manually:**

```bash
# Compile a .java file into bytecode (.class file)
javac HelloWorld.java

# Run the compiled program
java HelloWorld
```

---

## 3. Your First Program

```java
// HelloWorld.java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

**Breaking it down:**

| Part | Meaning |
|---|---|
| `public class HelloWorld` | Class name must match the filename (`HelloWorld.java`) |
| `public static void main(String[] args)` | Entry point — where the JVM starts execution |
| `System.out.println(...)` | Prints text to the console, followed by a newline |

---

## 4. Variables & Data Types

```java
public class DataTypes {
    public static void main(String[] args) {
        // Primitive data types
        int age = 25;                  // Whole numbers (32-bit)
        long population = 8_000_000_000L; // Larger whole numbers (64-bit, note the L suffix)
        double price = 19.99;           // Decimal numbers (64-bit)
        float temperature = 36.6f;      // Decimal numbers (32-bit, note the f suffix)
        boolean isActive = true;        // true or false
        char grade = 'A';               // A single character
        byte smallNumber = 127;         // -128 to 127
        short mediumNumber = 32000;     // -32,768 to 32,767

        // Reference type: String (not primitive, but used constantly)
        String name = "Sophea";

        // Constants (cannot be reassigned)
        final double PI = 3.14159;

        // Type inference (Java 10+)
        var city = "Phnom Penh"; // Compiler infers this is a String

        // Printing values
        System.out.println("Name: " + name + ", Age: " + age);
        System.out.printf("Price: $%.2f%n", price); // Formatted output

        // Type casting
        double d = 9.78;
        int i = (int) d; // Explicit cast: truncates to 9 (data loss)

        int x = 10;
        double y = x; // Implicit cast: int -> double (no data loss)
    }
}
```

---

## 5. Operators

```java
public class Operators {
    public static void main(String[] args) {
        // Arithmetic
        System.out.println(10 + 5);  // 15
        System.out.println(10 - 5);  // 5
        System.out.println(10 * 5);  // 50
        System.out.println(10 / 3);  // 3  (integer division truncates)
        System.out.println(10.0 / 3); // 3.333...
        System.out.println(10 % 3);  // 1  (remainder)

        // Increment/decrement
        int count = 0;
        count++;   // count = 1
        count--;   // count = 0
        ++count;   // Pre-increment: increments before use

        // Comparison
        System.out.println(5 == 5);   // true
        System.out.println(5 != 3);   // true
        System.out.println(5 > 3);    // true

        // Logical
        boolean a = true, b = false;
        System.out.println(a && b);   // false (AND)
        System.out.println(a || b);   // true  (OR)
        System.out.println(!a);       // false (NOT)

        // Ternary operator
        int score = 85;
        String result = (score >= 60) ? "Pass" : "Fail";

        // String comparison — ALWAYS use .equals(), never ==
        String s1 = "hello";
        String s2 = "hello";
        System.out.println(s1.equals(s2)); // true — correct way to compare content
        // s1 == s2 might be true or false depending on the string pool — don't rely on it
    }
}
```

---

## 6. Control Flow

```java
public class ControlFlow {
    public static void main(String[] args) {
        int score = 75;

        // if / else if / else
        if (score >= 90) {
            System.out.println("Grade: A");
        } else if (score >= 70) {
            System.out.println("Grade: B");
        } else {
            System.out.println("Grade: C or below");
        }

        // switch statement (traditional)
        int day = 3;
        switch (day) {
            case 1:
                System.out.println("Monday");
                break;
            case 2:
                System.out.println("Tuesday");
                break;
            default:
                System.out.println("Another day");
                break;
        }

        // switch expression (modern, Java 14+)
        String dayName = switch (day) {
            case 1 -> "Monday";
            case 2 -> "Tuesday";
            case 3 -> "Wednesday";
            default -> "Unknown";
        };
        System.out.println(dayName);

        // for loop
        for (int i = 0; i < 5; i++) {
            System.out.println("Iteration " + i);
        }

        // while loop
        int n = 0;
        while (n < 3) {
            System.out.println("n = " + n);
            n++;
        }

        // do-while loop (runs at least once)
        int m = 0;
        do {
            System.out.println("m = " + m);
            m++;
        } while (m < 3);

        // enhanced for-each loop (for arrays and collections)
        int[] numbers = {1, 2, 3, 4, 5};
        for (int num : numbers) {
            System.out.println(num);
        }

        // break and continue
        for (int i = 0; i < 10; i++) {
            if (i == 3) continue; // Skip this iteration
            if (i == 6) break;    // Exit the loop entirely
            System.out.println(i);
        }
    }
}
```

---

## 7. Arrays

```java
public class Arrays1 {
    public static void main(String[] args) {
        // Declaring and initializing arrays
        int[] numbers = {10, 20, 30, 40, 50};
        String[] names = new String[3]; // Array of size 3, all elements null
        names[0] = "Sophea";
        names[1] = "Dara";

        // Accessing elements
        System.out.println(numbers[0]);       // 10
        System.out.println(numbers.length);   // 5 (property, not a method)

        // Looping through an array
        for (int i = 0; i < numbers.length; i++) {
            System.out.println(numbers[i]);
        }

        // 2D arrays
        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };
        System.out.println(matrix[1][2]); // 6 (row 1, column 2)

        // Using java.util.Arrays utility methods
        int[] copy = java.util.Arrays.copyOf(numbers, numbers.length);
        java.util.Arrays.sort(numbers); // Sorts in place, ascending
        System.out.println(java.util.Arrays.toString(numbers)); // Readable print

        boolean contains = java.util.Arrays.asList(10, 20, 30).contains(20);
        System.out.println(contains); // true
    }
}
```

---

## 8. Methods

```java
public class Methods {

    // Basic method with a return value
    static int add(int a, int b) {
        return a + b;
    }

    // Void method — performs an action, returns nothing
    static void printGreeting(String name) {
        System.out.println("Hello, " + name + "!");
    }

    // Method overloading — same name, different parameters
    static double add(double a, double b) {
        return a + b;
    }

    // Varargs — accepts a variable number of arguments
    static int sum(int... numbers) {
        int total = 0;
        for (int n : numbers) {
            total += n;
        }
        return total;
    }

    // Recursive method
    static int factorial(int n) {
        if (n <= 1) return 1;          // Base case
        return n * factorial(n - 1);   // Recursive case
    }

    public static void main(String[] args) {
        System.out.println(add(3, 4));         // 7
        System.out.println(add(3.5, 4.2));     // 7.7 (overloaded version)
        printGreeting("Sophea");
        System.out.println(sum(1, 2, 3, 4, 5)); // 15
        System.out.println(factorial(5));       // 120
    }
}
```

---

## 9. OOP: Classes & Objects

```java
// Person.java
public class Person {
    // Fields (instance variables) — private for encapsulation
    private String name;
    private int age;

    // Constructor
    public Person(String name, int age) {
        this.name = name; // "this" refers to the current object's field
        this.age = age;
    }

    // Getters and setters (encapsulation — controlled access to fields)
    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        if (age < 0) {
            throw new IllegalArgumentException("Age cannot be negative");
        }
        this.age = age;
    }

    // Instance method
    public String introduce() {
        return "Hi, I'm " + name + " and I'm " + age + " years old.";
    }

    // Overriding Object's toString() for readable printing
    @Override
    public String toString() {
        return "Person{name='" + name + "', age=" + age + "}";
    }

    // Overriding equals() and hashCode() for correct comparison/collections use
    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;
        if (!(obj instanceof Person)) return false;
        Person other = (Person) obj;
        return age == other.age && name.equals(other.name);
    }

    @Override
    public int hashCode() {
        return java.util.Objects.hash(name, age);
    }
}
```

```java
// Main.java
public class Main {
    public static void main(String[] args) {
        Person p1 = new Person("Sophea", 25);
        System.out.println(p1.introduce());     // Hi, I'm Sophea and I'm 25 years old.
        System.out.println(p1);                  // Person{name='Sophea', age=25}

        p1.setAge(26);
        System.out.println(p1.getAge());          // 26

        Person p2 = new Person("Sophea", 26);
        System.out.println(p1.equals(p2));        // true (same name & age)
    }
}
```

**Java records (modern, concise data classes — Java 16+):**

```java
// Immutable data class in one line — auto-generates constructor, getters, equals, hashCode, toString
public record PersonRecord(String name, int age) { }
```

```java
PersonRecord p = new PersonRecord("Dara", 30);
System.out.println(p.name()); // "Dara" — auto-generated accessor
System.out.println(p);        // PersonRecord[name=Dara, age=30]
```

---

## 10. Inheritance & Polymorphism

```java
// Animal.java — base/parent class
public class Animal {
    protected String name;

    public Animal(String name) {
        this.name = name;
    }

    public String makeSound() {
        return name + " makes a sound";
    }
}
```

```java
// Dog.java — subclass/child class
public class Dog extends Animal {
    private String breed;

    public Dog(String name, String breed) {
        super(name); // Call the parent class's constructor
        this.breed = breed;
    }

    @Override // Overriding the parent's method
    public String makeSound() {
        return name + " barks! (a " + breed + ")";
    }

    public String fetch() {
        return name + " fetches the ball!";
    }
}
```

```java
public class Main {
    public static void main(String[] args) {
        Animal genericAnimal = new Animal("Creature");
        System.out.println(genericAnimal.makeSound()); // "Creature makes a sound"

        Dog dog = new Dog("Rex", "Golden Retriever");
        System.out.println(dog.makeSound()); // "Rex barks! (a Golden Retriever)"
        System.out.println(dog.fetch());

        // Polymorphism — a Dog IS-A Animal, so this reference type works
        Animal polymorphicDog = new Dog("Max", "Poodle");
        System.out.println(polymorphicDog.makeSound()); // Calls Dog's overridden version

        // instanceof check
        if (polymorphicDog instanceof Dog) {
            System.out.println("This animal is a dog");
        }
    }
}
```

---

## 11. Interfaces & Abstract Classes

```java
// Interface — a contract of methods a class must implement
public interface Payable {
    double calculatePayment(); // Abstract method — no body

    // Default method (Java 8+) — has a body, classes can use it as-is or override
    default String describe() {
        return "This entity is payable.";
    }
}
```

```java
// Abstract class — a partial implementation, cannot be instantiated directly
public abstract class Employee {
    protected String name;

    public Employee(String name) {
        this.name = name;
    }

    // Abstract method — must be implemented by subclasses
    public abstract double calculateSalary();

    // Concrete method — shared by all subclasses
    public String getName() {
        return name;
    }
}
```

```java
// FullTimeEmployee.java — implements both the abstract class and an interface
public class FullTimeEmployee extends Employee implements Payable {
    private double monthlySalary;

    public FullTimeEmployee(String name, double monthlySalary) {
        super(name);
        this.monthlySalary = monthlySalary;
    }

    @Override
    public double calculateSalary() {
        return monthlySalary;
    }

    @Override
    public double calculatePayment() {
        return calculateSalary();
    }
}
```

```java
public class Main {
    public static void main(String[] args) {
        FullTimeEmployee emp = new FullTimeEmployee("Sophea", 1500.0);
        System.out.println(emp.getName() + ": $" + emp.calculateSalary());
        System.out.println(emp.describe()); // Uses the interface's default method
    }
}
```

**Interface vs abstract class:**

| | Interface | Abstract Class |
|---|---|---|
| Instantiable? | No | No |
| Multiple inheritance | A class can implement many interfaces | A class can extend only one abstract class |
| Fields | Only `public static final` constants | Any field type, any visibility |
| Method bodies | Only `default`/`static` methods have bodies | Any method can have a body |

---

## 12. Exception Handling

```java
public class ExceptionHandling {

    static int divide(int a, int b) {
        if (b == 0) {
            throw new ArithmeticException("Cannot divide by zero");
        }
        return a / b;
    }

    public static void main(String[] args) {
        // try / catch / finally
        try {
            int result = divide(10, 0);
            System.out.println(result);
        } catch (ArithmeticException e) {
            System.out.println("Error: " + e.getMessage());
        } finally {
            System.out.println("This always runs, error or not");
        }

        // Catching multiple exception types
        try {
            int[] arr = new int[5];
            arr[10] = 1; // Throws ArrayIndexOutOfBoundsException
        } catch (ArrayIndexOutOfBoundsException | NullPointerException e) {
            System.out.println("Caught: " + e.getMessage());
        }

        // try-with-resources — automatically closes resources (e.g. files, streams)
        try (java.io.BufferedReader reader = new java.io.BufferedReader(
                new java.io.FileReader("data.txt"))) {
            System.out.println(reader.readLine());
        } catch (java.io.IOException e) {
            System.out.println("File error: " + e.getMessage());
        }

        // Custom exceptions
        try {
            validateAge(-5);
        } catch (InvalidAgeException e) {
            System.out.println("Validation failed: " + e.getMessage());
        }
    }

    static void validateAge(int age) throws InvalidAgeException {
        if (age < 0) {
            throw new InvalidAgeException("Age cannot be negative: " + age);
        }
    }
}

// Custom checked exception
class InvalidAgeException extends Exception {
    public InvalidAgeException(String message) {
        super(message);
    }
}
```

**Checked vs unchecked exceptions:**

| Type | Examples | Must be declared/caught? |
|---|---|---|
| Checked | `IOException`, `SQLException` | Yes — compiler enforces it |
| Unchecked (RuntimeException) | `NullPointerException`, `ArithmeticException` | No — optional |

---

## 13. Collections Framework

```java
import java.util.*;

public class Collections1 {
    public static void main(String[] args) {

        // --- List (ordered, allows duplicates) ---
        List<String> fruits = new ArrayList<>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Apple"); // Duplicates allowed
        fruits.remove("Banana");
        System.out.println(fruits);                // [Apple, Apple]
        System.out.println(fruits.contains("Apple")); // true
        System.out.println(fruits.get(0));           // Apple

        List<Integer> linkedList = new LinkedList<>(); // Better for frequent insert/delete

        // --- Set (no duplicates) ---
        Set<String> uniqueNames = new HashSet<>();     // No guaranteed order
        uniqueNames.add("Sophea");
        uniqueNames.add("Sophea"); // Ignored — already exists
        System.out.println(uniqueNames.size()); // 1

        Set<String> sortedSet = new TreeSet<>(); // Automatically sorted
        sortedSet.add("banana");
        sortedSet.add("apple");
        System.out.println(sortedSet); // [apple, banana]

        // --- Map (key-value pairs) ---
        Map<String, Integer> ages = new HashMap<>();
        ages.put("Sophea", 25);
        ages.put("Dara", 30);
        ages.put("Sophea", 26); // Overwrites the previous value

        System.out.println(ages.get("Sophea"));        // 26
        System.out.println(ages.getOrDefault("Unknown", 0)); // 0 (fallback)
        System.out.println(ages.containsKey("Dara"));    // true

        for (Map.Entry<String, Integer> entry : ages.entrySet()) {
            System.out.println(entry.getKey() + " is " + entry.getValue());
        }

        Map<String, Integer> sortedMap = new TreeMap<>(ages); // Sorted by key

        // --- Queue (FIFO — first in, first out) ---
        Queue<String> queue = new LinkedList<>();
        queue.offer("First");
        queue.offer("Second");
        System.out.println(queue.poll()); // "First" — removes and returns the head

        // --- Deque (double-ended queue — can act as a stack too) ---
        Deque<Integer> stack = new ArrayDeque<>();
        stack.push(1);
        stack.push(2);
        System.out.println(stack.pop()); // 2 (LIFO — last in, first out)
    }
}
```

---

## 14. Generics

```java
// A generic class — works with any type, decided at usage time
public class Box<T> {
    private T content;

    public void set(T content) {
        this.content = content;
    }

    public T get() {
        return content;
    }
}
```

```java
public class GenericsDemo {
    // Generic method
    static <T> void printArray(T[] array) {
        for (T item : array) {
            System.out.println(item);
        }
    }

    // Bounded type parameter — T must be a Number or subclass
    static <T extends Number> double sumAll(List<T> numbers) {
        double sum = 0;
        for (T n : numbers) {
            sum += n.doubleValue();
        }
        return sum;
    }

    public static void main(String[] args) {
        Box<String> stringBox = new Box<>();
        stringBox.set("Hello");
        System.out.println(stringBox.get()); // "Hello"

        Box<Integer> intBox = new Box<>();
        intBox.set(42);
        System.out.println(intBox.get()); // 42

        Integer[] numbers = {1, 2, 3};
        printArray(numbers);

        List<Integer> ints = List.of(1, 2, 3, 4);
        System.out.println(sumAll(ints)); // 10.0

        // Wildcards
        List<? extends Number> readOnlyNumbers = ints; // Accepts any Number subtype, read-only
    }
}
```

---

## 15. Streams & Lambda Expressions

```java
import java.util.*;
import java.util.stream.*;

public class StreamsDemo {

    record Product(String name, double price, boolean inStock) { }

    public static void main(String[] args) {
        List<Product> products = List.of(
            new Product("Laptop", 1200, true),
            new Product("Mouse", 25, true),
            new Product("Monitor", 300, false),
            new Product("Keyboard", 75, true)
        );

        // Lambda expressions — a compact way to write a function inline
        Comparator<Product> byPrice = (p1, p2) -> Double.compare(p1.price(), p2.price());

        // filter + map + collect
        List<String> inStockNames = products.stream()
            .filter(p -> p.inStock())
            .map(Product::name)              // Method reference — shorthand for p -> p.name()
            .collect(Collectors.toList());
        System.out.println(inStockNames); // [Laptop, Mouse, Keyboard]

        // sorted
        List<Product> sortedByPrice = products.stream()
            .sorted(byPrice)
            .collect(Collectors.toList());

        // reduce — combine into a single value
        double totalPrice = products.stream()
            .mapToDouble(Product::price)
            .sum();
        System.out.println(totalPrice); // 1600.0

        // count, min, max
        long inStockCount = products.stream().filter(Product::inStock).count();
        Optional<Product> cheapest = products.stream().min(byPrice);
        cheapest.ifPresent(p -> System.out.println("Cheapest: " + p.name()));

        // anyMatch / allMatch
        boolean hasExpensive = products.stream().anyMatch(p -> p.price() > 1000);
        boolean allInStock = products.stream().allMatch(Product::inStock);

        // grouping
        Map<Boolean, List<Product>> groupedByStock = products.stream()
            .collect(Collectors.groupingBy(Product::inStock));

        // Functional interfaces used with lambdas
        Runnable task = () -> System.out.println("Task running");
        task.run();

        java.util.function.Function<Integer, Integer> square = n -> n * n;
        System.out.println(square.apply(5)); // 25

        java.util.function.Predicate<Integer> isEven = n -> n % 2 == 0;
        System.out.println(isEven.test(4)); // true
    }
}
```

---

## 16. File I/O

```java
import java.io.*;
import java.nio.file.*;
import java.util.List;

public class FileIODemo {
    public static void main(String[] args) throws IOException {

        // --- Writing to a file (modern NIO API — recommended) ---
        Path path = Paths.get("output.txt");
        Files.writeString(path, "Hello, File I/O!\nSecond line.");

        // --- Reading an entire file as a String ---
        String content = Files.readString(path);
        System.out.println(content);

        // --- Reading all lines into a List ---
        List<String> lines = Files.readAllLines(path);
        for (String line : lines) {
            System.out.println(line);
        }

        // --- Appending to a file ---
        Files.writeString(path, "\nAppended line", StandardOpenOption.APPEND);

        // --- Traditional BufferedReader/Writer (still widely used) ---
        try (BufferedWriter writer = new BufferedWriter(new FileWriter("log.txt"))) {
            writer.write("Log entry 1");
            writer.newLine();
            writer.write("Log entry 2");
        }

        try (BufferedReader reader = new BufferedReader(new FileReader("log.txt"))) {
            String line;
            while ((line = reader.readLine()) != null) {
                System.out.println(line);
            }
        }

        // --- Checking if a file exists ---
        System.out.println(Files.exists(path)); // true

        // --- Deleting a file ---
        Files.deleteIfExists(Paths.get("log.txt"));
    }
}
```

---

## 17. Multithreading Basics

```java
public class ThreadingDemo {

    // A simple task implementing Runnable
    static class PrintTask implements Runnable {
        private final String message;

        PrintTask(String message) {
            this.message = message;
        }

        @Override
        public void run() {
            for (int i = 0; i < 3; i++) {
                System.out.println(message + " - " + i);
            }
        }
    }

    public static void main(String[] args) throws InterruptedException {

        // Creating and starting threads
        Thread t1 = new Thread(new PrintTask("Thread A"));
        Thread t2 = new Thread(new PrintTask("Thread B"));
        t1.start();
        t2.start();

        // Waiting for threads to finish
        t1.join();
        t2.join();

        // Using a lambda instead of a Runnable class
        Thread t3 = new Thread(() -> System.out.println("Running from a lambda thread"));
        t3.start();

        // ExecutorService — modern, managed thread pool (preferred over raw Threads)
        java.util.concurrent.ExecutorService executor =
            java.util.concurrent.Executors.newFixedThreadPool(2);

        executor.submit(() -> System.out.println("Task 1 running"));
        executor.submit(() -> System.out.println("Task 2 running"));

        executor.shutdown(); // Always shut down the pool when done

        // Synchronization — preventing race conditions on shared data
        Counter counter = new Counter();
        Thread inc1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) counter.increment();
        });
        Thread inc2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) counter.increment();
        });
        inc1.start();
        inc2.start();
        inc1.join();
        inc2.join();
        System.out.println("Final count: " + counter.getCount()); // Always 2000
    }

    static class Counter {
        private int count = 0;

        // synchronized prevents two threads from modifying `count` at the same time
        public synchronized void increment() {
            count++;
        }

        public int getCount() {
            return count;
        }
    }
}
```

---

## 18. Best Practices

- ✅ Follow Java naming conventions: `ClassName` (PascalCase), `methodName`/`variableName` (camelCase), `CONSTANT_NAME` (UPPER_SNAKE_CASE)
- ✅ Keep fields `private` and expose behavior through public methods (encapsulation)
- ✅ Always compare objects (especially `String`) with `.equals()`, never `==`
- ✅ Override `equals()` and `hashCode()` together, never just one
- ✅ Prefer interfaces (`List`, `Map`) as variable types over concrete classes (`ArrayList`, `HashMap`)
- ✅ Use try-with-resources for anything that implements `AutoCloseable` (files, streams, connections)
- ✅ Favor immutability where possible — use `final` fields and records for data carriers
- ✅ Use `Optional<T>` for methods that might not return a value, instead of returning `null`
- ✅ Use `ExecutorService` instead of managing raw `Thread` objects manually
- ✅ Write unit tests with **JUnit** for all non-trivial logic

---

## 19. Full Example Project

A simple **Library Management** system combining OOP, collections, exceptions, and streams:

```java
// Book.java
public record Book(String title, String author, boolean available) { }
```

```java
// BookNotFoundException.java
public class BookNotFoundException extends RuntimeException {
    public BookNotFoundException(String title) {
        super("Book not found: " + title);
    }
}
```

```java
// Library.java
import java.util.*;
import java.util.stream.*;

public class Library {
    private final List<Book> books = new ArrayList<>();

    public void addBook(Book book) {
        books.add(book);
    }

    public Book findByTitle(String title) {
        return books.stream()
            .filter(b -> b.title().equalsIgnoreCase(title))
            .findFirst()
            .orElseThrow(() -> new BookNotFoundException(title));
    }

    public List<Book> getAvailableBooks() {
        return books.stream()
            .filter(Book::available)
            .collect(Collectors.toList());
    }

    public Map<String, List<Book>> groupByAuthor() {
        return books.stream()
            .collect(Collectors.groupingBy(Book::author));
    }

    public void printCatalog() {
        books.forEach(b ->
            System.out.println(b.title() + " by " + b.author() +
                (b.available() ? " [Available]" : " [Checked Out]")));
    }
}
```

```java
// Main.java
public class Main {
    public static void main(String[] args) {
        Library library = new Library();
        library.addBook(new Book("Effective Java", "Joshua Bloch", true));
        library.addBook(new Book("Clean Code", "Robert Martin", false));
        library.addBook(new Book("Java Concurrency", "Brian Goetz", true));

        library.printCatalog();

        System.out.println("\nAvailable books:");
        library.getAvailableBooks().forEach(b -> System.out.println(b.title()));

        try {
            Book found = library.findByTitle("Clean Code");
            System.out.println("\nFound: " + found);

            library.findByTitle("Unknown Book"); // Throws BookNotFoundException
        } catch (BookNotFoundException e) {
            System.out.println("\nError: " + e.getMessage());
        }
    }
}
```

---

## 20. Resources

- Official docs: `https://docs.oracle.com/en/java/`
- Java tutorials: `https://docs.oracle.com/javase/tutorial/`
- OpenJDK: `https://openjdk.org/`

---

<p align="center">
  Made with ❤️ for developers learning Java.
</p>
