# ☕ ការផ្តើមសិក្សា Java - ពីប្រឹក្សាដល់ឈានល្ងាច

![Java](https://img.shields.io/badge/Java-17+-red?style=flat-square&logo=java)
![Difficulty](https://img.shields.io/badge/Level-Beginner%20to%20Advanced-blue?style=flat-square)
![Language](https://img.shields.io/badge/Language-Khmer%20ខ្មែរ-green?style=flat-square)

---

## 📋 តារាងមាតិកា

1. [Java](#java)
2. [បរិស្ថាននៃការងារ](#បរិស្ថាននៃការងារ)
3. [ក្រូច្ចូលដង](#ក្រូច្ចូលដង)
4. [ប្រភេទទិន្នន័យ](#ប្រភេទទិន្នន័យ)
5. [អនុគមន៍](#អនុគមន៍)
6. [ទិន្នន័យលម្អិត](#ទិន្នន័យលម្អិត)
7. [OOP](#oop-programming)
8. [Exception Handling](#exception-handling)
9. [Collections](#collections)
10. [File I/O](#file-io)

---

## 🎯 Java

### ❓ Java ជាអ្វី?

**Java** គឺជាភាសាសរសេរកម្មវិធីដែលមានលក្ខណៈពិសេស៖

- 🔄 **Object-Oriented** - វាផ្នែកខ្លួនឯងលើ classes និង objects
- 🌍 **Platform Independent** - "រៀបចំម្តងប្រើរឹង" (Write Once, Run Anywhere - WORA)
- 💪 **Strongly Typed** - ត្រូវកំណត់ប្រភេទទិន្នន័យច្បាស់លាស់
- 🛡️ **Secure** - មានលក្ខណៈសម្រាប់សុវត្ថិភាព
- 🚀 **High Performance** - រលឿននិងមានប្រសិទ្ធភាព

### 🔗 របូបនៃលំហូរ

```
ឯកសារ Java (.java)
        ↓
    Compiler
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
1. JDK (Java Development Kit) - ក្របីផ្នែក
   - JRE (Java Runtime Environment)
   - Compiler
   - ឧបករណ៍អស់រលុង

2. Text Editor ឬ IDE
   - IntelliJ IDEA (រូបដ៏ល្អបំផុត)
   - Eclipse
   - Visual Studio Code
   - NetBeans

3. Command Line / Terminal
```

### ✅ ឆ្លងកាត់ការដំឡើង

```bash
# ពិនិត្យលេខ Java
java -version

# ពិនិត្យ Compiler
javac -version
```

---

## 💻 ក្រូច្ចូលដង (Hello World)

### ឧទាហរណ៍សម្រាប់ដំបូង

```java
public class HelloWorld {
    // main method - ចូលក្នុងដែលជាបឋមនៃផ្នែក
    public static void main(String[] args) {
        System.out.println("សួស្តីលោក ពិភពលោក!");
    }
}
```

### 📝 ការពន្យល់លម្អិត

| ផ្នែក | អត្ថន័យ |
|------|---------|
| `public` | មើលឃើញគ្រប់ដែល |
| `class HelloWorld` | ឈ្មោះក្រុង |
| `static` | អាចហៅដោយគ្មាន instance |
| `void` | មិនផ្តល់តម្លៃ |
| `main(String[] args)` | ចូលក្នុងដែល |
| `System.out.println()` | បោះពុម្ពលទ្ធផល |

### ▶️ របូបរត់

```bash
# Compile
javac HelloWorld.java

# រត់
java HelloWorld

# លទ្ធផល
សួស្តីលោក ពិភពលោក!
```

---

## 📊 ប្រភេទទិន្នន័យ

### 1️⃣ Primitive Data Types

ប្រភេទទិន្នន័យដែលចាប់ផ្តើមតូចបំផុត៖

#### ចំនួនគត់ (Integer Types)

```java
byte byteValue = 127;           // -128 ទៅ 127
short shortValue = 32000;       // -32,768 ទៅ 32,767
int intValue = 2147483647;      // ធម្មតាប្រើ
long longValue = 9223372036854775807L; // ដូច្នេះធំ (L)

// ឧទាហរណ៍
int age = 25;
int count = 100;
```

#### ចំនួនលេខ (Floating Point)

```java
float floatValue = 3.14f;       // តូច (f)
double doubleValue = 3.14159;   // ធម្មតាប្រើ (ធំ)

// ឧទាហរណ៍
float price = 99.99f;
double pi = 3.14159265359;
```

#### ពិតឬក្លាយ (Boolean)

```java
boolean isTrue = true;
boolean isFalse = false;

// ឧទាហរណ៍
boolean isActive = true;
boolean isEmpty = false;
```

#### អក្សរតែមួយ (Character)

```java
char letter = 'A';
char digit = '5';
char special = '@';

// ឧទាហរណ៍
char initial = 'J';
```

### 2️⃣ Reference Data Types

ប្រភេទទិន្នន័យដែលលឹងឆ្ងាយ៖

#### String - អក្សរលេខ

```java
String name = "សូចា";
String message = "សួស្តីលោក";
String empty = "";

// ប្រើប្រាស់
String greeting = "សួស្តីលោក " + name;
System.out.println(greeting);  // សួស្តីលោក សូចា
```

#### Array - ឈានល្ងាច

```java
// ប្រភេទមូលដ្ឋាន
int[] numbers = {1, 2, 3, 4, 5};
String[] fruits = {"ផ្លែប៉ោម", "ក្រូច", "ផ្លែឈើ"};

// ដែលគ្មានកម្មវិធីប្រឹក្សា
int[] emptyArray = new int[10];

// ប្រើប្រាស់
System.out.println(numbers[0]); // 1
System.out.println(fruits[1]); // ក្រូច
```

### 📋 ឧទាហរណ៍ពង្រីក

```java
public class DataTypesExample {
    public static void main(String[] args) {
        // ចំនួនគត់
        int age = 25;
        long population = 8000000000L;
        
        // ចំនួនលេខ
        double salary = 5000.50;
        
        // ពិតឬក្លាយ
        boolean isStudent = true;
        
        // អក្សរ
        String name = "ដាវីដ";
        char grade = 'A';
        
        // បោះពុម្ព
        System.out.println("ឈ្មោះ: " + name);
        System.out.println("អាយុ: " + age);
        System.out.println("ថ្នាក់: " + grade);
        System.out.println("ប្រាក់ឈានលើកតែមួយ: " + salary);
        System.out.println("ជាសិស្ស: " + isStudent);
    }
}
```

---

## 🔄 អនុគមន៍

### 1️⃣ អនុគមន៍មូលដ្ឋាន

```java
// ឧទាហរណ៍ 1: អនុគមន៍មិនផ្តល់តម្លៃ
public static void greet() {
    System.out.println("សួស្តីលោក!");
}

// ឧទាហរណ៍ 2: អនុគមន៍ដែលផ្តល់តម្លៃ
public static int add(int a, int b) {
    return a + b;
}

// ឧទាហរណ៍ 3: អនុគមន៍ដែលមានប៉ារ៉ាម៉ែត្រ
public static void printInfo(String name, int age) {
    System.out.println("ឈ្មោះ: " + name + ", អាយុ: " + age);
}
```

### 2️⃣ ការហៅអនុគមន៍

```java
public class FunctionExample {
    
    // អនុគមន៍គណនាការេនៃលេខ
    public static int square(int number) {
        return number * number;
    }
    
    // អនុគមន៍បង្ហាញព័ត៌មាន
    public static void showUserInfo(String name, int age, double salary) {
        System.out.println("=== ព័ត៌មានអ្នកប្រើប្រាស់ ===");
        System.out.println("ឈ្មោះ: " + name);
        System.out.println("អាយុ: " + age);
        System.out.println("ប្រាក់ឈានលើកតែមួយ: " + salary);
    }
    
    public static void main(String[] args) {
        // ហៅអនុគមន៍
        int result = square(5);
        System.out.println("5² = " + result);  // 25
        
        showUserInfo("សូចា", 30, 5000);
    }
}
```

### 3️⃣ Overloading

```java
// អនុគមន៍ដដែលឈ្មោះ ប៉ុន្តែផ្សេងគ្នា parameter
public static int add(int a, int b) {
    return a + b;
}

public static double add(double a, double b) {
    return a + b;
}

public static String add(String a, String b) {
    return a + b;
}

// ការប្រើប្រាស់
System.out.println(add(5, 10));           // 15
System.out.println(add(5.5, 10.5));       // 16.0
System.out.println(add("សួស្តី", "លោក")); // សួស្តីលោក
```

---

## 🎮 ទិន្នន័យលម្អិត

### 1️⃣ ប្រកាសលក្ខខណ្ឌ (If-Else)

```java
public class ConditionExample {
    public static void main(String[] args) {
        int age = 18;
        
        // ប្រកាសលក្ខខណ្ឌ IF
        if (age >= 18) {
            System.out.println("អ្នកមានលក្ខណៈលក្ខ");
        }
        
        // IF-ELSE
        if (age < 18) {
            System.out.println("អ្នកក្មេង");
        } else {
            System.out.println("អ្នកធំ");
        }
        
        // IF-ELSE IF-ELSE
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

### 2️⃣ ចូលក្នុងប្រកាស (Switch)

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
        
        System.out.println("ថ្ងៃដែលស្មើនឹង: " + dayName);
    }
}
```

### 3️⃣ រង្វិលជុំ (Loops)

#### FOR Loop

```java
public class ForLoopExample {
    public static void main(String[] args) {
        // រង្វិលជុំ FOR ធម្មតា
        System.out.println("=== FOR LOOP ===");
        for (int i = 1; i <= 5; i++) {
            System.out.println("លេខ: " + i);
        }
        
        // រង្វិលជុំលើ Array
        System.out.println("\n=== Array Loop ===");
        int[] numbers = {10, 20, 30, 40, 50};
        for (int i = 0; i < numbers.length; i++) {
            System.out.println("នៅទីតាំង " + i + ": " + numbers[i]);
        }
        
        // Enhanced FOR Loop (foreach)
        System.out.println("\n=== Enhanced FOR ===");
        for (int num : numbers) {
            System.out.println("លេខ: " + num);
        }
    }
}
```

#### WHILE Loop

```java
public class WhileLoopExample {
    public static void main(String[] args) {
        // WHILE LOOP
        int count = 1;
        while (count <= 3) {
            System.out.println("រាប់: " + count);
            count++;
        }
        
        // DO-WHILE (រត់យ៉ាងហោចណាស់ម្តង)
        System.out.println("\n=== DO-WHILE ===");
        int num = 1;
        do {
            System.out.println("លេខ: " + num);
            num++;
        } while (num <= 3);
    }
}
```

### 4️⃣ ប្រតិបត្តិកម្ម

```java
public class OperatorsExample {
    public static void main(String[] args) {
        int a = 10, b = 5;
        
        // ប្រតិបត្តិកម្មរឹម
        System.out.println("a + b = " + (a + b));  // 15
        System.out.println("a - b = " + (a - b));  // 5
        System.out.println("a * b = " + (a * b));  // 50
        System.out.println("a / b = " + (a / b));  // 2
        System.out.println("a % b = " + (a % b));  // 0
        
        // ប្រតិបត្តិកម្មប្រៀបធៀប
        System.out.println("\n=== ប្រៀបធៀប ===");
        System.out.println("a > b: " + (a > b));   // true
        System.out.println("a == b: " + (a == b)); // false
        System.out.println("a != b: " + (a != b)); // true
        
        // ប្រតិបត្តិកម្មលូហ៊ីក
        System.out.println("\n=== លូហ៊ីក ===");
        boolean x = true, y = false;
        System.out.println("x && y: " + (x && y)); // false
        System.out.println("x || y: " + (x || y)); // true
        System.out.println("!x: " + (!x));         // false
    }
}
```

---

## 🏗️ OOP Programming

ការផ្តើមសិក្សា Object-Oriented Programming

### 1️⃣ Class និង Object

```java
// កំណត់ក្រុង (Blueprint)
public class Car {
    // Attributes (លក្ខណៈ)
    public String brand;
    public String color;
    public int year;
    
    // Constructor (ការផ្តើមនៃលក្ខណៈ)
    public Car(String brand, String color, int year) {
        this.brand = brand;
        this.color = color;
        this.year = year;
    }
    
    // Methods (អនុគមន៍)
    public void displayInfo() {
        System.out.println("ម៉ាក: " + brand);
        System.out.println("ពណ៌: " + color);
        System.out.println("ឆ្នាំ: " + year);
    }
    
    public void drive() {
        System.out.println(brand + " កំពុងដ្ឋាននាពេលលើ");
    }
}

// ការប្រើប្រាស់
public class Main {
    public static void main(String[] args) {
        // បង្កើត object
        Car myCar = new Car("Toyota", "ក្រហម", 2020);
        
        // ហៅ methods
        myCar.displayInfo();
        myCar.drive();
    }
}
```

### 2️⃣ Encapsulation

```java
public class Student {
    // Private attributes
    private String name;
    private double gpa;
    
    // Public methods (Getters & Setters)
    public String getName() {
        return name;
    }
    
    public void setName(String name) {
        if (name != null && !name.isEmpty()) {
            this.name = name;
        }
    }
    
    public double getGpa() {
        return gpa;
    }
    
    public void setGpa(double gpa) {
        if (gpa >= 0 && gpa <= 4.0) {
            this.gpa = gpa;
        }
    }
    
    // Method ដែលដាក់ស្មារទ្ធិក
    public String getGradeLevel() {
        if (gpa >= 3.5) return "A";
        if (gpa >= 3.0) return "B";
        if (gpa >= 2.0) return "C";
        return "F";
    }
}

// ការប្រើប្រាស់
Student student = new Student();
student.setName("សូចា");
student.setGpa(3.8);
System.out.println("ឈ្មោះ: " + student.getName());
System.out.println("ថ្នាក់: " + student.getGradeLevel()); // A
```

### 3️⃣ Inheritance

```java
// ក្រុងមា (Parent Class)
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

// ក្រុងកូន (Child Class)
public class Dog extends Animal {
    public Dog(String name) {
        super(name); // ហៅ constructor របស់ parent
    }
    
    @Override
    public void eat() {
        System.out.println(name + " កំពុងញ៉ាំសាច់");
    }
    
    // Method ថ្មី
    public void bark() {
        System.out.println(name + " ឪឡ ឪឡ!");
    }
}

// ការប្រើប្រាស់
Dog dog = new Dog("បង់ក");
dog.eat();    // បង់ក កំពុងញ៉ាំសាច់
dog.sleep();  // បង់ក កំពុងដេក
dog.bark();   // បង់ក ឪឡ ឪឡ!
```

### 4️⃣ Polymorphism

```java
// Interface (ស្ថានីយកម្មលម្អិត)
public interface Animal {
    void makeSound();
    void move();
}

// ការអនុវត្ត
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

// ការប្រើប្រាស់
Animal cat = new Cat();
Animal dog = new Dog();

cat.makeSound();  // ម៉ៀវ ម៉ៀវ!
dog.makeSound();  // ឆ្នូត ឆ្នូត!
```

---

## ⚠️ Exception Handling

### 1️⃣ Try-Catch

```java
public class ExceptionExample {
    public static void main(String[] args) {
        try {
            // កូដដែលអាចឬបាន
            String text = "សួស្តី";
            int number = Integer.parseInt(text); // Error!
            
        } catch (NumberFormatException e) {
            // ចាប់អាក្រក្តកូអាច
            System.out.println("កំហុស: មិនអាចបម្លែងទៅលេខបាន");
            System.out.println("មូលហេតុ: " + e.getMessage());
            
        } catch (Exception e) {
            // ប្រឹក្សាដ្ឋានទូទៅ
            System.out.println("មានកំហុស: " + e.getMessage());
        }
    }
}
```

### 2️⃣ Try-Catch-Finally

```java
public class FileHandlingExample {
    public static void main(String[] args) {
        try {
            // ងាកូដលម្អិត
            int result = 10 / 0;
            
        } catch (ArithmeticException e) {
            System.out.println("មិនអាចចែកបានលេខសូន្យ!");
            
        } finally {
            // រត់ក្នុងករណីទាំងមូល
            System.out.println("Finally block រត់វង់");
        }
    }
}
```

### 3️⃣ Throws

```java
public class ThrowsExample {
    
    public static void readFile(String filename) throws Exception {
        if (filename == null) {
            throw new Exception("ឈ្មោះឯកសារមិនអាចគ្មាននោះ");
        }
        System.out.println("កំពុងអាន: " + filename);
    }
    
    public static void main(String[] args) {
        try {
            readFile(null);
        } catch (Exception e) {
            System.out.println("កំហុស: " + e.getMessage());
        }
    }
}
```

---

## 📦 Collections

### 1️⃣ ArrayList

```java
import java.util.ArrayList;

public class ArrayListExample {
    public static void main(String[] args) {
        // បង្កើត ArrayList
        ArrayList<String> fruits = new ArrayList<>();
        
        // បន្ថែម
        fruits.add("ផ្លែប៉ោម");
        fruits.add("ក្រូច");
        fruits.add("ផ្លែឈើ");
        
        // ឯកសារលម្អិត
        System.out.println("ចំនួន: " + fruits.size());        // 3
        System.out.println("ឧទាហរណ៍ 0: " + fruits.get(0));    // ផ្លែប៉ោម
        
        // ផ្លាស់ប្តូរ
        fruits.set(1, "ម្នាស");
        
        // ដក
        fruits.remove(2);
        
        // លង្វង់
        for (String fruit : fruits) {
            System.out.println("- " + fruit);
        }
    }
}
```

### 2️⃣ HashMap

```java
import java.util.HashMap;

public class HashMapExample {
    public static void main(String[] args) {
        // បង្កើត HashMap
        HashMap<String, Integer> ages = new HashMap<>();
        
        // បន្ថែម
        ages.put("សូចា", 25);
        ages.put("ដាវីដ", 30);
        ages.put("សារ៉ា", 28);
        
        // ទទួលបាន
        System.out.println("អាយុរបស់សូចា: " + ages.get("សូចា"));
        
        // ឆែក
        if (ages.containsKey("ដាវីដ")) {
            System.out.println("ដាវីដ មាននៅក្នុង map");
        }
        
        // លង្វង់
        for (String key : ages.keySet()) {
            System.out.println(key + ": " + ages.get(key));
        }
    }
}
```

### 3️⃣ HashSet

```java
import java.util.HashSet;

public class HashSetExample {
    public static void main(String[] args) {
        // បង្កើត HashSet (គ្មានលេខស្ទួន)
        HashSet<Integer> numbers = new HashSet<>();
        
        // បន្ថែម
        numbers.add(10);
        numbers.add(20);
        numbers.add(10); // មិនរាប់ម្តង
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

## 📁 File I/O

### 1️⃣ អាន​ឯកសារ

```java
import java.io.File;
import java.io.FileReader;
import java.io.BufferedReader;
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
            System.out.println("កំហុសក្នុងការអាន: " + e.getMessage());
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
            writer.write("នេះគឺលើកដំបូង។");
            
            writer.close();
            System.out.println("ឯកសារបានសរសេរដោយរីករាយ");
            
        } catch (IOException e) {
            System.out.println("កំហុស: " + e.getMessage());
        }
    }
}
```

---

## 🚀 ឧទាហរណ៍ប្រឹក្សាមួយ

```java
import java.util.ArrayList;
import java.util.Scanner;

/**
 * សមាជិកគ្រប់គ្រង (Student Management System)
 * 
 * លក្ខណៈពិសេស:
 * - បន្ថែមសមាជិក
 * - បង្ហាញព័ត៌មាន
 * - ស្វែងរកសមាជិក
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

// ក្រុងផ្ទាល់ខ្លួន
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
        return "សិស្ស{" +
                "ឈ្មោះ='" + name + '\'' +
                ", អាយុ=" + age +
                ", GPA=" + gpa +
                '}';
    }
}
```

---

## 📚 ល្បច និងដំណាក់កាល

### ✅ ល្បច

```java
// 1. ប្រើ final សម្រាប់ constants
final int MAX_USERS = 100;

// 2. ប្រើ null check
if (string != null && !string.isEmpty()) {
    // ដំណើរការ
}

// 3. ប្រើ try-with-resources
try (BufferedReader reader = new BufferedReader(new FileReader("file.txt"))) {
    // អាន
} catch (IOException e) {
    e.printStackTrace();
}

// 4. ប្រើ StringBuilder សម្រាប់ string concatenation
StringBuilder sb = new StringBuilder();
sb.append("សួស្តី");
sb.append(" ");
sb.append("លោក");
String result = sb.toString();
```

### ❌ ដែលមិនគួរ

```java
// ១. មិនប្រើ raw types
// ❌ ArrayList list = new ArrayList();
// ✅ ArrayList<String> list = new ArrayList<>();

// ២. មិនលើកលែងលម្អិត
// ❌ catch (Exception e) { }
// ✅ catch (SpecificException e) { }

// ៣. មិនចាប់ផ្តើម null ដោយប្រើមាន
// ❌ if (object == null || object.method()) { }
// ✅ if (object != null && object.method()) { }
```

---

## 🎓 សង្ខេប

| ប្រធានបទ | ស្តាប់រ |
|---------|--------|
| **ផ្នែក** | ក្រុង, object, attribute |
| **ដែលលាក់** | private, protected, public |
| **អនុគមន៍** | method ដែលបង្ហាញអាកម្ម |
| **Inheritance** | ក្រុងកូនខ្លួនក្រុងមា |
| **Polymorphism** | ច្រើនលក្ខណៈលម្អិត |
| **Interface** | ឧបករណ៍ក្រាលលម្អិត |
| **Exception** | ប្រឹក្សាដ្ឋាននៃកំហុស |
| **Collections** | ArrayList, HashMap, HashSet |

---

<details>
<summary><b>📌 ឧទាហរណ៍ពេញលេញ (អាចលាក់)</b></summary>

```java
public class CompleteExample {
    
    interface Shape {
        double getArea();
        void display();
    }
    
    static class Rectangle implements Shape {
        private double width, height;
        
        public Rectangle(double width, double height) {
            this.width = width;
            this.height = height;
        }
        
        @Override
        public double getArea() {
            return width * height;
        }
        
        @Override
        public void display() {
            System.out.println("ចតុកោណ - ធំ: " + getArea());
        }
    }
    
    static class Circle implements Shape {
        private double radius;
        
        public Circle(double radius) {
            this.radius = radius;
        }
        
        @Override
        public double getArea() {
            return Math.PI * radius * radius;
        }
        
        @Override
        public void display() {
            System.out.println("រង្វង់ - ធំ: " + getArea());
        }
    }
    
    public static void main(String[] args) {
        ArrayList<Shape> shapes = new ArrayList<>();
        shapes.add(new Rectangle(5, 10));
        shapes.add(new Circle(7));
        
        for (Shape shape : shapes) {
            shape.display();
        }
    }
}
```

</details>

---

## 🔗 ធនធានលម្អិត

- [Oracle Java Documentation](https://docs.oracle.com/en/java/)
- [Java Tutorials](https://docs.oracle.com/javase/tutorial/)
- [GeeksforGeeks Java](https://www.geeksforgeeks.org/java/)

---

## 🎉 រួចរាល់!

> [!TIP]
> អនុវត្តការសរសេរកូដជារៀងរាល់ថ្ងៃ! សូមបង្កើតគម្រោងតូចដើម្បីក្សាន់ការយល់ដឹងរបស់អ្នក។

---

**ឯកសារលម្អិត:** 2024 | **ស្ថិតិ:** 🟢 ស្វាគមន៍ | **បែប:** Khmer 🇰🇭

ឡើងលើក្នុងលម្អិត ហើយរីករាយក្នុងការសរសេរកម្មវិធី! ☕💻
