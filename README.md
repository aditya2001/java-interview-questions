# Java Basics

## 1. Explain the main idea behind _Java_ and the concept of _Write Once, Run Anywhere_.
Java is platform independent ,object-oriented programming language. 
1. Byte code - Java source code is complied into platform-independent byte code which can be executed by an JVM.
Java byte code can be executed on any device with a compatible JVM from smartphones to computer.
2. JVM - Java virtual machine has its own run time environment which executes byte code. JVM is platform dependent, because every
operating environment has its own JVM. 



## 2. What are the main features of Java?
1. Platform Independent- Write once, run anywhere.
2. Object-Oriented- Emphasizes on classes and objects, therefore promoting OOPS concepts.
3. Secure - Java programs runs inside a virtual machine, therefore it's secure.


## 3. Difference between JDK, JVM and JRE?

JVM-
1. JVM Interprets Java byte code into machine specific instructions
2. Memory Management - Handles memory management include garbage collection.
3. JIT compilation - Converts byte code to machine code.
4. Exception Handling - Manages exception handling.

JRE-
The JRE (Java Runtime Environment) is the minimum environment required to execute a Java application.

JDK-
JDK includes development kit, providing everything need to for java application development.
javac: The Java compiler
java: The Java application launcher

# Java Wrapper Classes

## 4. Can you explain the difference between an int and an Integer in Java?

#### int
- **Primitive data type**
- Memory allocation: Fixed $32$ bits (or $4$ bytes)
- Instantiation: Direct, no constructor required
- Default value: $0$
- Performance: Generally faster due to direct value storage

#### Integer
- **Wrapper class** for the primitive `int`
- Provides additional functionality via class methods
- Memory allocation: Variable, typically more than `int`
- Instantiation: Through constructor, auto-boxing, or `valueOf()`
- Default value: `null` (if not assigned)
- Performance: Slightly slower due to object overhead

## 5. What are _wrapper classes_ in _Java_?

**Wrapper classes** in Java allow you to work with primitive data types as objects. They are particularly useful when working with generic collections or when using features that require objects, such as **Java Bean properties**.

Wrapper classes not only provide a way to convert primitives to and from objects but also offer various utility methods specific to each primitive type.

### Core Wrapper Classes

| Primitive | Wrapper Class | Conversion Methods | Primitive Example | Wrapper Example |
| --- | --- | --- | --- | --- |
| `boolean` | `Boolean` | `.valueOf()` <br> `.parseBoolean()` <br> `.booleanValue()` | `true` | `Boolean.TRUE` |
| `byte` | `Byte` | `.valueOf()` <br> `.parseByte()` <br> `.byteValue()` | `123` | `Byte.valueOf((byte)123)` |
| `char` | `Character` | `.valueOf()` <br> `.charValue()` | `'a'` | `Character.valueOf('a')` |
| `short` | `Short` | `.valueOf()` <br> `.parseShort()` <br> `.shortValue()` | `123` | `Short.valueOf((short)123)` |
| `int` | `Integer` | `.valueOf()` <br> `.parseInt()` <br> `.intValue()` | `123` | `Integer.valueOf(123)` |
| `long` | `Long` | `.valueOf()` <br> `.parseLong()` <br> `.longValue()` | `123L` | `Long.valueOf(123L)` |
| `float` | `Float` | `.valueOf()` <br> `.parseFloat()` <br> `.floatValue()` | `123.45f` | `Float.valueOf(123.45f)` |
| `double` | `Double` | `.valueOf()` <br> `.parseDouble()` <br> `.doubleValue()` | `123.45` | `Double.valueOf(123.45)` |

### Use Cases for Wrapper Classes

#### 1. Collections

Generic collections in Java require objects, not primitives. Wrapper classes allow you to use primitives in these collections.

```java
List<Integer> numbers = new ArrayList<>();
numbers.add(5);  // Autoboxing: int to Integer
int num = numbers.get(0);  // Unboxing: Integer to int
```

#### 2. Nullability

Wrapper classes can represent the absence of a value using `null`, which primitives cannot.

```java
Integer age = null;  // Valid
int primitiveAge = null;  // Compilation error
```

#### 4. Utility Methods

Wrapper classes provide useful utility methods for their respective types.

```java
String binaryString = Integer.toBinaryString(42);
int maxValue = Integer.MAX_VALUE;
boolean isDigit = Character.isDigit('7');
```
<br>

# Object-Oriented Basics

## 6. Is _Java_ a pure _object-oriented language_? Why or why not?

Java is **not** a pure object-oriented language. While it incorporates many object-oriented programming (OOP) principles, it retains some elements from procedural programming.

### Object-Oriented Features in Java

Java supports the four main pillars of OOP:

1. **Encapsulation**: Achieved through access modifiers (`public`, `private`, `protected`).
2. **Abstraction**: Implemented via abstract classes and interfaces.
3. **Inheritance**: Supported using the `extends` keyword for classes and `implements` for interfaces.
4. **Polymorphism**: Realized through method overloading and overriding.

### Non-Pure OOP Elements in Java

1. **Primitive Data Types**: Java includes non-object primitives like `int`, `boolean`, `char`, etc.

2. **Static Members**: The `static` keyword allows for class-level fields and methods, not tied to object instances.

3. **Procedural Constructs**: Java supports procedural programming elements such as control flow statements (`if`, `for`, `while`, etc.).

### Code Example: Mixed OOP and Non-OOP Features

```java
public class Example {
    private int instanceVar;  // Encapsulation: private instance variable
    public static int staticVar = 10;  // Static variable

    public void instanceMethod() {
        // Procedural construct
        if (instanceVar > 5) {
            System.out.println("Greater than 5");
        }
    }

    public static void main(String[] args) {
        int localVar = 20;  // Primitive type
        Example obj = new Example();
        obj.instanceMethod();  // OOP: method invocation on object
        System.out.println(Example.staticVar);  // Accessing static member
    }
}
```
<br>


# Strings

## Why are String immutable in Java?
##### String are immutable in java means, once a String object is created it cannot be modified.
##### String pool is only possible because of immutable behavior.Different String variables can refer to same object in pool.
##### Since String is immutable, it is safe for multithreading. A single String instance can be shared across different threads.

# Object-Oriented Concepts

# Collections

# Exception Handling 

# MultiThreading

 







