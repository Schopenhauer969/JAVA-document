# ☕ ការផ្តើមសិក្សា Java - ពីប្រឹក្សាដល់ឈានល្ងាច

![Java](https://img.shields.io/badge/Java-17+-red?style=flat-square&logo=java)
![Difficulty](https://img.shields.io/badge/Level-Beginner%20to%20Advanced-blue?style=flat-square)
![Language](https://img.shields.io/badge/Language-Khmer%20ខ្មែរ-green?style=flat-square)

---

## 📋 តារាងមាតិកា

1. [ឈានល្ងាច Java](#ឈានល្ងាច-java)
2. [បរិស្ថាននៃការងារ](#បរិស្ថាននៃការងារ)
3. [Hello World](#hello-world)
4. [ប្រភេទទិន្នន័យ](#ប្រភេទទិន្នន័យ)
5. [អនុគមន៍](#អនុគមន៍)
6. [ទិន្នន័យលម្អិត](#ទិន្នន័យលម្អិត)
7. [OOP Concepts](#oop-concepts)
8. [Exception Handling](#exception-handling)
9. [Collections](#collections)
10. [File I/O](#file-io)

---

## 🎯 ឈានល្ងាច Java

### ❓ Java ជាអ្វី?

**Java** គឺជាភាសាសរសេរកម្មវិធីដែលមានលក្ខណៈពិសេស៖

- 🔄 **Object-Oriented** - ផ្នែកខ្លួនឯងលើ objects និង classes
- 🌍 **Platform Independent** - សរសេរម្តង រត់ everywhere (WORA)
- 💪 **Strongly Typed** - ត្រូវកំណត់ data types ច្បាស់លាស់
- 🛡️ **Secure** - មានលក្ខណៈសម្រាប់សុវត្ថិភាព
- 🚀 **High Performance** - រលឿននិងមានប្រសិទ្ធភាព

### 🔗 របូបនៃលំហូរ

```
Java Source File (.java)
        ↓
    Compiler (javac)
        ↓
Java Bytecode (.class)
        ↓
    JVM (Java Virtual Machine)
        ↓
    លទ្ធផល
```

---

## 🛠️ បរិស្ថាននៃការងារ

### 📥 តម្រូវការ

```
1. JDK (Java Development Kit)
   - JRE (Java Runtime Environment)
   - javac Compiler
   - ឧបករណ៍មូលដ្ឋាន

2. IDE (Integrated Development Environment)
   - IntelliJ IDEA (ល្អបំផុត)
   - Eclipse
   - Visual Studio Code
   - NetBeans

3. Command Line / Terminal
```

### ✅ ឆ្លងកាត់ការដំឡើង

```bash
# ពិនិត្យ Java version
java -version

# ពិនិត្យ Compiler version
javac -version
```

---

## 💻 Hello World

### ឧទាហរណ៍សម្រាប់ដំបូង

```java
public class HelloWorld {
    // main method - ចូលក្នុងដែលបឋមនៃផ្នែក
    public static void main(String[] args) {
        System.out.println("សួស្តីលោក ពិភពលោក!");
    }
}
```

### 📝 ការពន្យល់លម្អិត

| Keyword | អត្ថន័យ |
|---------|---------|
| `public` | មើលឃើញច្រើនទាំងអស់ |
| `class` | ក្រុង/template សម្រាប់ object |
| `static` | ក្រុងមាឯង មិនត្រូវ instance |
| `void` | method មិនបង្ហាញតម្លៃ |
| `main(String[] args)` | ចូលក្នុងដែលដែលកម្មវិធីចាប់ផ្តើម |
| `System.out.println()` | បោះពុម្ពលទ្ធផលដល់ console |

### ▶️ របូបរត់

```bash
# Step 1: Compile file
javac HelloWorld.java

# Step 2: Run the program
java HelloWorld

# លទ្ធផល:
សួស្តីលោក ពិភពលោក!
```

---

## 📊 ប្រភេទទិន្នន័យ

### 1️⃣ Primitive Data Types

ប្រភេទទិន្នន័យមូលដ្ឋាននៅក្នុង Java

#### Integer Types (ចំនួនគត់)

```java
byte byteVar = 127;              // -128 ទៅ 127
short shortVar = 32000;          // -32,768 ទៅ 32,767
int intVar = 2147483647;         // ធម្មតាប្រើបំផុត
long longVar = 9223372036854775807L; // ធំ (ដាក់ L នៅចុង)

// ឧទាហរណ៍ការប្រើ
int age = 25;
int count = 100;
long population = 8000000000L;
```

#### Floating Point Types (ចំនួនលេខទសភាគ)

```java
float floatVar = 3.14f;          // តូច (ដាក់ f នៅចុង)
double doubleVar = 3.14159265;   // ធម្មតាប្រើបំផុត

// ឧទាហរណ៍
float price = 99.99f;
double pi = 3.14159265359;
double salary = 5000.50;
```

#### Boolean Type (ពិតឬមិនពិត)

```java
boolean isTrue = true;
boolean isFalse = false;

// ឧទាហរណ៍
boolean isActive = true;
boolean isEmpty = false;
boolean isAdmin = true;
```

#### Character Type (អក្សរតែមួយ)

```java
char letter = 'A';
char digit = '5';
char special = '@';

// ឧទាហរណ៍
char initial = 'J';
char symbol = '#';
```

### 2️⃣ Reference Data Types

ប្រភេទទិន្នន័យខ្លាំង/ស្មុគស្មាញ

#### String (ឃ្នាលេខលេខ)

```java
String name = "សូចា";
String message = "សួស្តីលោក";
String empty = "";

// ប្រើប្រាស់ String
String greeting = "សួស្តីលោក " + name;
System.out.println(greeting);  // សួស្តីលោក សូចា

// String methods
int length = name.length();
String upper = name.toUpperCase();
boolean contains = greeting.contains("សូចា");
```

#### Array (ឈានល្ងាច)

```java
// ប្រភេទមូលដ្ឋាន
int[] numbers = {1, 2, 3, 4, 5};
String[] fruits = {"ផ្លែប៉ោម", "ក្រូច", "ផ្លែឈើ"};

// ដែលគ្មានតម្លៃដំបូង (default 0 or null)
int[] emptyArray = new int[10];
String[] nameArray = new String[5];

// ប្រើប្រាស់
System.out.println(numbers[0]);    // 1
System.out.println(fruits[1]);     // ក្រូច
System.out.println(numbers.length); // 5

// ផ្លាស់ប្តូរតម្លៃ
numbers[0] = 10;
```

### 📋 ឧទាហរណ៍ពង្រីក

```java
public class DataTypesExample {
    public static void main(String[] args) {
        // Integer types
        int age = 25;
        long population = 8000000000L;
        
        // Floating point
        double salary = 5000.50;
        float discount = 15.5f;
        
        // Boolean
        boolean isStudent = true;
        boolean isWorking = false;
        
        // Character
        char grade = 'A';
        
        // String
        String name = "ដាវីដ";
        String city = "ក្រុងភ្នំពេញ";
        
        // បោះពុម្ព
        System.out.println("ឈ្មោះ: " + name);
        System.out.println("អាយុ: " + age);
        System.out.println("ថ្នាក់: " + grade);
        System.out.println("ប្រាក់ឈានលើកតែមួយ: " + salary);
        System.out.println("ឃ្នាលេខលេខ: " + city);
    }
}
```

---

## 🔄 អនុគមន៍ (Methods/Functions)

### 1️⃣ អនុគមន៍មូលដ្ឋាន

```java
// ឧទាហរណ៍ 1: void method (មិនផ្តល់តម្លៃ)
public static void greet() {
    System.out.println("សួស្តីលោក!");
}

// ឧទាហរណ៍ 2: return method
public static int add(int a, int b) {
    return a + b;  // ផ្តល់តម្លៃ
}

// ឧទាហរណ៍ 3: method ដែលមាន parameters
public static void printInfo(String name, int age) {
    System.out.println("ឈ្មោះ: " + name);
    System.out.println("អាយុ: " + age);
}
```

### 2️⃣ ការហៅ methods

```java
public class MethodExample {
    
    // method ដែលគណនាក្នុង square
    public static int square(int number) {
        return number * number;
    }
    
    // method ដែលបង្ហាញព័ត៌មាន
    public static void showUserInfo(String name, int age, double salary) {
        System.out.println("=== ព័ត៌មាននៃ User ===");
        System.out.println("ឈ្មោះ: " + name);
        System.out.println("អាយុ: " + age);
        System.out.println("ប្រាក់ឈានលើកតែមួយ: " + salary);
    }
    
    // method ដែលតម្រើញលេខធំបំផុត
    public static int findMax(int a, int b) {
        return (a > b) ? a : b;
    }
    
    public static void main(String[] args) {
        // ហៅ methods
        int result = square(5);
        System.out.println("5² = " + result);  // 25
        
        showUserInfo("សូចា", 30, 5000);
        
        int max = findMax(10, 20);
        System.out.println("លេខធំបំផុត: " + max);  // 20
    }
}
```

### 3️⃣ Method Overloading

```java
// method ដែលមាន overloading (ឈ្មោះដូច ប៉ុន្តែ parameters ខុស)
public static int add(int a, int b) {
    return a + b;
}

public static double add(double a, double b) {
    return a + b;
}

public static String add(String a, String b) {
    return a + b;  // concatenate
}

// ការប្រើប្រាស់
System.out.println(add(5, 10));              // 15 (int)
System.out.println(add(5.5, 10.5));          // 16.0 (double)
System.out.println(add("សួស្តី", " លោក")); // សួស្តី លោក (String)
```

---

## 🎮 ទិន្នន័យលម្អិត (Control Flow)

### 1️⃣ ប្របាស់ប្រកាស (If-Else)

```java
public class IfElseExample {
    public static void main(String[] args) {
        int age = 18;
        
        // ប្របាស់ IF ឯកលេខ
        if (age >= 18) {
            System.out.println("អ្នកមានលក្ខណៈលក្ខ");
        }
        
        // IF-ELSE (មាន 2 ផ្លូវ)
        if (age < 18) {
            System.out.println("អ្នកក្មេង");
        } else {
            System.out.println("អ្នកធំ");
        }
        
        // IF-ELSE IF-ELSE (មាន 3+ ផ្លូវ)
        if (age < 13) {
            System.out.println("កុមារ");
        } else if (age < 18) {
            System.out.println("យុវជន");
        } else if (age < 60) {
            System.out.println("មនុស្សពេញលេញ");
        } else {
            System.out.println("មនុស្សចាស់");
        }
    }
}
```

### 2️⃣ ប្របាស់ Switch (ផ្លូវច្រើន)

```java
public class SwitchExample {
    public static void main(String[] args) {
        int day = 3;
        String dayName;
        
        switch (day) {
            case 1:
                dayName = "ច័ន្ទ";
                break;
            case 2:
                dayName = "អង្គារ";
                break;
            case 3:
                dayName = "ពុធ";
                break;
            case 4:
                dayName = "ព្រហស្បតិ៍";
                break;
            case 5:
                dayName = "សុក្រ";
                break;
            case 6:
                dayName = "សៅរ៍";
                break;
            case 7:
                dayName = "អាទិត្យ";
                break;
            default:
                dayName = "ថ្ងៃមិនស្គាល់";
        }
        
        System.out.println("ថ្ងៃ: " + dayName);
    }
}
```

### 3️⃣ រង្វិលជុំ (Loops)

#### for Loop

```java
public class ForLoopExample {
    public static void main(String[] args) {
        // for loop ធម្មតា
        System.out.println("=== FOR LOOP ===");
        for (int i = 1; i <= 5; i++) {
            System.out.println("លេខ: " + i);
        }
        
        // loop លើ array
        System.out.println("\n=== ARRAY LOOP ===");
        int[] numbers = {10, 20, 30, 40, 50};
        for (int i = 0; i < numbers.length; i++) {
            System.out.println("Index " + i + ": " + numbers[i]);
        }
        
        // enhanced for loop (foreach)
        System.out.println("\n=== ENHANCED FOR ===");
        for (int num : numbers) {
            System.out.println("លេខ: " + num);
        }
    }
}
```

#### while Loop

```java
public class WhileLoopExample {
    public static void main(String[] args) {
        // while loop
        System.out.println("=== WHILE LOOP ===");
        int count = 1;
        while (count <= 3) {
            System.out.println("រាប់: " + count);
            count++;
        }
        
        // do-while (រត់យ៉ាងហោចណាស់ម្តង)
        System.out.println("\n=== DO-WHILE ===");
        int num = 1;
        do {
            System.out.println("លេខ: " + num);
            num++;
        } while (num <= 3);
    }
}
```

### 4️⃣ Operators (ប្រតិបត្តិកម្ម)

```java
public class OperatorsExample {
    public static void main(String[] args) {
        int a = 10, b = 5;
        
        // Arithmetic operators (ដកូលគណិត)
        System.out.println("a + b = " + (a + b));  // 15
        System.out.println("a - b = " + (a - b));  // 5
        System.out.println("a * b = " + (a * b));  // 50
        System.out.println("a / b = " + (a / b));  // 2
        System.out.println("a % b = " + (a % b));  // 0
        
        // Comparison operators (ប្របាស់ប្រៀបធៀប)
        System.out.println("\n=== Comparison ===");
        System.out.println("a > b: " + (a > b));   // true
        System.out.println("a < b: " + (a < b));   // false
        System.out.println("a == b: " + (a == b)); // false
        System.out.println("a != b: " + (a != b)); // true
        
        // Logical operators (ឡូហ្សីក)
        System.out.println("\n=== Logical ===");
        boolean x = true, y = false;
        System.out.println("x && y: " + (x && y)); // false (AND)
        System.out.println("x || y: " + (x || y)); // true (OR)
        System.out.println("!x: " + (!x));         // false (NOT)
        
        // Assignment operators (ផ្តល់តម្លៃ)
        int c = 10;
        c += 5;   // c = c + 5 (15)
        c -= 3;   // c = c - 3 (12)
        c *= 2;   // c = c * 2 (24)
    }
}
```

---

## 🏗️ OOP Concepts

Object-Oriented Programming គឺជាគោលគំនិតដ៏សំខាន់នៃ Java

### 1️⃣ Class និង Object

```java
// ស្ថាបនា class (blueprint)
public class Car {
    // Attributes (ឯកតា)
    public String brand;
    public String color;
    public int year;
    
    // Constructor (ផ្តើមដំបូង)
    public Car(String brand, String color, int year) {
        this.brand = brand;
        this.color = color;
        this.year = year;
    }
    
    // Methods (អនុគមន៍/កម្មវិធី)
    public void displayInfo() {
        System.out.println("ម៉ាក: " + brand);
        System.out.println("ពណ៌: " + color);
        System.out.println("ឆ្នាំ: " + year);
    }
    
    public void drive() {
        System.out.println(brand + " កំពុងដ្ឋាននាពេលលើ");
    }
    
    public void stop() {
        System.out.println(brand + " ឈប់");
    }
}

// ការប្រើប្រាស់
public class Main {
    public static void main(String[] args) {
        // បង្កើត object (instance)
        Car myCar = new Car("Toyota", "ក្រហម", 2020);
        
        // ហៅ methods
        myCar.displayInfo();
        myCar.drive();
        myCar.stop();
    }
}
```

### 2️⃣ Encapsulation (ការលាក់ទុក)

```java
public class Student {
    // private - មិនអាចចូលដោយផ្ទាល់
    private String name;
    private double gpa;
    
    // Getters - ដើម្បីទទួលតម្លៃ
    public String getName() {
        return name;
    }
    
    public double getGpa() {
        return gpa;
    }
    
    // Setters - ដើម្បីកំណត់តម្លៃ (ដោយលក្ខខណ្ឌ)
    public void setName(String name) {
        if (name != null && !name.isEmpty()) {
            this.name = name;
        }
    }
    
    public void setGpa(double gpa) {
        // ត្រូវលក្ខណៈលក្ខ 0-4.0
        if (gpa >= 0 && gpa <= 4.0) {
            this.gpa = gpa;
        }
    }
    
    // Business logic
    public String getGradeLevel() {
        if (gpa >= 3.5) return "A";
        if (gpa >= 3.0) return "B";
        if (gpa >= 2.0) return "C";
        return "F";
    }
}

// ការប្រើ
Student student = new Student();
student.setName("សូចា");
student.setGpa(3.8);
System.out.println("ឈ្មោះ: " + student.getName());
System.out.println("ថ្នាក់: " + student.getGradeLevel()); // A
```

### 3️⃣ Inheritance (ការបន្ត/មរតក)

```java
// Parent class (ក្រុងមា)
public class Animal {
    protected String name;
    
    public Animal(String name) {
        this.name = name;
    }
    
    public void eat() {
        System.out.println(name + " កំពុងញ៉ាំ");
    }
    
    public void sleep() {
        System.out.println(name + " កំពុងដេក");
    }
}

// Child class (ក្រុងកូន) - សង្វាក់
public class Dog extends Animal {
    public Dog(String name) {
        super(name); // ហៅ parent constructor
    }
    
    // Override (ធ្វើឡើងវិញ) method មាន
    @Override
    public void eat() {
        System.out.println(name + " កំពុងញ៉ាំសាច់");
    }
    
    // Method ថ្មីរបស់ Dog
    public void bark() {
        System.out.println(name + " ឪឡ ឪឡ!");
    }
}

// ការប្រើ
Dog myDog = new Dog("បង់ក");
myDog.eat();    // បង់ក កំពុងញ៉ាំសាច់
myDog.sleep();  // បង់ក កំពុងដេក
myDog.bark();   // បង់ក ឪឡ ឪឡ!
```

### 4️⃣ Polymorphism (ច្រើនម៉ាត)

```java
// Interface (កម្មវិធីលម្អិត)
public interface Animal {
    void makeSound();
    void move();
}

// Implementation 1
public class Cat implements Animal {
    @Override
    public void makeSound() {
        System.out.println("ម៉ៀវ ម៉ៀវ!");
    }
    
    @Override
    public void move() {
        System.out.println("ឃ្មុំកំពុងដើរលឿង");
    }
}

// Implementation 2
public class Dog implements Animal {
    @Override
    public void makeSound() {
        System.out.println("ឆ្នូត ឆ្នូត!");
    }
    
    @Override
    public void move() {
        System.out.println("ឆ្នាប់កំពុងដើរយឺត");
    }
}

// ការប្រើ
Animal cat = new Cat();
Animal dog = new Dog();

cat.makeSound();  // ម៉ៀវ ម៉ៀវ!
dog.makeSound();  // ឆ្នូត ឆ្នូត!
```

---

## ⚠️ Exception Handling

ការគ្រប់គ្រងកំហុស

### 1️⃣ Try-Catch

```java
public class ExceptionExample {
    public static void main(String[] args) {
        try {
            // កូដដែលអាច throw exception
            String text = "សួស្តី";
            int number = Integer.parseInt(text); // Error!
            
        } catch (NumberFormatException e) {
            // ចាប់កំហុស specific
            System.out.println("កំហុស: មិនអាចបម្លែងទៅលេខ");
            System.out.println("សារ: " + e.getMessage());
            
        } catch (Exception e) {
            // ចាប់ exception ទូទៅ
            System.out.println("មានកំហុស: " + e.getMessage());
        }
    }
}
```

### 2️⃣ Try-Catch-Finally

```java
public class TryCatchFinallyExample {
    public static void main(String[] args) {
        try {
            int result = 10 / 0;  // ArithmeticException
            
        } catch (ArithmeticException e) {
            System.out.println("មិនអាចចែកលេខសូន្យ!");
            
        } finally {
            // ដំណើរការក្នុងករណីទាំងអស់
            System.out.println("Finally block រត់ក្នុងលើក");
        }
    }
}
```

### 3️⃣ Throws Keyword

```java
public class ThrowsExample {
    
    public static void readFile(String filename) throws Exception {
        if (filename == null) {
            throw new Exception("Filename cannot be null");
        }
        System.out.println("Reading: " + filename);
    }
    
    public static void main(String[] args) {
        try {
            readFile(null);
        } catch (Exception e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

---

## 📦 Collections

### 1️⃣ ArrayList (អរេ Dynamics)

```java
import java.util.ArrayList;

public class ArrayListExample {
    public static void main(String[] args) {
        // បង្កើត ArrayList
        ArrayList<String> fruits = new ArrayList<>();
        
        // បន្ថែម (add)
        fruits.add("ផ្លែប៉ោម");
        fruits.add("ក្រូច");
        fruits.add("ផ្លែឈើ");
        
        // ពត៌មាន
        System.out.println("ចំនួន: " + fruits.size());        // 3
        System.out.println("Index 0: " + fruits.get(0));      // ផ្លែប៉ោម
        
        // កែប្រែ (modify)
        fruits.set(1, "ម្នាស");
        
        // លុប (remove)
        fruits.remove(2);
        
        // រង្វិលជុំ
        for (String fruit : fruits) {
            System.out.println("- " + fruit);
        }
    }
}
```

### 2️⃣ HashMap (ផែនទីលេខ)

```java
import java.util.HashMap;

public class HashMapExample {
    public static void main(String[] args) {
        // បង្កើត HashMap (Key-Value pair)
        HashMap<String, Integer> ages = new HashMap<>();
        
        // បន្ថែម
        ages.put("សូចា", 25);
        ages.put("ដាវីដ", 30);
        ages.put("សារ៉ា", 28);
        
        // ទទួលបាន
        System.out.println("អាយុរបស់សូចា: " + ages.get("សូចា"));
        
        // ឆែក (contain)
        if (ages.containsKey("ដាវីដ")) {
            System.out.println("ដាវីដ មាននៅក្នុង map");
        }
        
        // រង្វិលជុំ
        for (String key : ages.keySet()) {
            System.out.println(key + ": " + ages.get(key));
        }
    }
}
```

### 3️⃣ HashSet (សំណុំលេខ)

```java
import java.util.HashSet;

public class HashSetExample {
    public static void main(String[] args) {
        // បង្កើត HashSet (គ្មានលេខស្ទួន)
        HashSet<Integer> numbers = new HashSet<>();
        
        // បន្ថែម
        numbers.add(10);
        numbers.add(20);
        numbers.add(10); // មិនបន្ថែម (duplicate)
        numbers.add(30);
        
        System.out.println("ចំនួន: " + numbers.size()); // 3
        
        // ឆែក
        if (numbers.contains(20)) {
            System.out.println("20 មាននៅក្នុង set");
        }
    }
}
```

---

## 📁 File I/O (អាន-សរសេរឯកសារ)

### 1️⃣ អានឯកសារ

```java
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class FileReadExample {
    public static void main(String[] args) {
        try {
            BufferedReader reader = new BufferedReader(
                new FileReader("sample.txt")
            );
            
            String line;
            while ((line = reader.readLine()) != null) {
                System.out.println(line);
            }
            
            reader.close();
            
        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

### 2️⃣ សរសេរឯកសារ

```java
import java.io.FileWriter;
import java.io.IOException;

public class FileWriteExample {
    public static void main(String[] args) {
        try {
            FileWriter writer = new FileWriter("output.txt");
            
            writer.write("សួស្តីលោក ពិភពលោក!\n");
            writer.write("នេះគឺឯកសារដែលសរសេរដោយ Java");
            
            writer.close();
            System.out.println("ឯកសារបានសរសេរដោយរីករាយ");
            
        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

---

## 🚀 ឧទាហរណ៍ប្រឹក្សាពេញលេញ

```java
import java.util.ArrayList;
import java.util.Scanner;

/**
 * Student Management System
 * 
 * Features:
 * - Add students
 * - Display students
 * - Search students
 */
public class StudentManagementSystem {
    
    public static void main(String[] args) {
        ArrayList<Student> students = new ArrayList<>();
        Scanner scanner = new Scanner(System.in);
        boolean running = true;
        
        while (running) {
            System.out.println("\n=== ប្រព័ន្ធគ្រប់គ្រងសិស្ស ===");
            System.out.println("1. បន្ថែមសិស្ស");
            System.out.println("2. បង្ហាញសិស្សទាំងអស់");
            System.out.println("3. ស្វែងរកសិស្ស");
            System.out.println("4. ចាកចេញ");
            System.out.print("ជ្រើសរើស: ");
            
            int choice = scanner.nextInt();
            scanner.nextLine(); // Clear buffer
            
            switch (choice) {
                case 1:
                    System.out.print("ឈ្មោះ: ");
                    String name = scanner.nextLine();
                    System.out.print("អាយុ: ");
                    int age = scanner.nextInt();
                    System.out.print("GPA: ");
                    double gpa = scanner.nextDouble();
                    
                    students.add(new Student(name, age, gpa));
                    System.out.println("✅ បានបន្ថែមដោយរីករាយ");
                    break;
                    
                case 2:
                    if (students.isEmpty()) {
                        System.out.println("គ្មានសិស្សនៅក្នុង");
                    } else {
                        for (int i = 0; i < students.size(); i++) {
                            System.out.println((i + 1) + ". " + students.get(i));
                        }
                    }
                    break;
                    
                case 3:
                    System.out.print("ស្វែងរកឈ្មោះ: ");
                    String searchName = scanner.nextLine();
                    boolean found = false;
                    
                    for (Student student : students) {
                        if (student.getName().equalsIgnoreCase(searchName)) {
                            System.out.println("រកឃើញ: " + student);
                            found = true;
                            break;
                        }
                    }
                    
                    if (!found) {
                        System.out.println("មិនរកឃើញសិស្ស");
                    }
                    break;
                    
                case 4:
                    running = false;
                    System.out.println("សូមបង្ហាញសំណេក!");
                    break;
                    
                default:
                    System.out.println("❌ ជ្រើសរើសមិនប្រាកដ");
            }
        }
        
        scanner.close();
    }
}

// Student Class
class Student {
    private String name;
    private int age;
    private double gpa;
    
    public Student(String name, int age, double gpa) {
        this.name = name;
        this.age = age;
        this.gpa = gpa;
    }
    
    public String getName() {
        return name;
    }
    
    @Override
    public String toString() {
        return "Student{" +
                "name='" + name + '\'' +
                ", age=" + age +
                ", gpa=" + gpa +
                '}';
    }
}
```

---

## 📚 Best Practices & Tips

### ✅ ល្បច (Do's)

```java
// 1. Use final សម្រាប់ constants
final int MAX_USERS = 100;

// 2. null check មុនប្រើ
if (string != null && !string.isEmpty()) {
    // process
}

// 3. try-with-resources (Auto close)
try (BufferedReader reader = new BufferedReader(
        new FileReader("file.txt"))) {
    // read file
} catch (IOException e) {
    e.printStackTrace();
}

// 4. StringBuilder សម្រាប់ string concatenation
StringBuilder sb = new StringBuilder();
sb.append("Hello");
sb.append(" ");
sb.append("World");
String result = sb.toString();
```

### ❌ មិនគួរ (Don'ts)

```java
// 1. មិនប្រើ raw types
// ❌ ArrayList list = new ArrayList();
// ✅ ArrayList<String> list = new ArrayList<>();

// 2. មិនចាប់ Exception generic
// ❌ catch (Exception e) { }
// ✅ catch (SpecificException e) { }

// 3. មិនប្រើ == សម្រាប់ String comparison
// ❌ if (str1 == str2) { }
// ✅ if (str1.equals(str2)) { }
```

---

## 🎓 សង្ខេប Concepts

| Concept | អត្ថន័យ |
|---------|---------|
| **class** | Template សម្រាប់ objects |
| **object** | Instance របស់ class |
| **method** | Function នៅក្នុង class |
| **attribute** | Variable នៅក្នុង class |
| **constructor** | Special method ដែលផ្តើម object |
| **inheritance** | Class ច្រើន extends one parent |
| **polymorphism** | One interface, multiple forms |
| **encapsulation** | Hide internal details |
| **interface** | Contract សម្រាប់ classes |
| **exception** | Error handling mechanism |

---

## 🔗 Resources

- [Oracle Java Documentation](https://docs.oracle.com/en/java/)
- [Java Tutorials](https://docs.oracle.com/javase/tutorial/)
- [GeeksforGeeks Java](https://www.geeksforgeeks.org/java/)

---

## 🎉 ចុងក្រោយ

> [!TIP]
> ការអនុវត្តការសរសេរកូដជារៀងរាល់ថ្ងៃ! ព្យាយាមបង្កើតគម្រោងតូចដើម្បីក្សាន់ការយល់ដឹងរបស់អ្នក។

---

**ឯកសារលម្អិត:** 2024 | **Status:** 🟢 Active | **Language:** Khmer ខ្មែរ

ឡើងលើក្នុងលម្អិត ហើយរីករាយក្នុងការសរសេរកម្មវិធី! ☕💻
