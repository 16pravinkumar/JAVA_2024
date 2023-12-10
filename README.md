# All about JAVA File Structure
A java program can contain any number of classes but atmost one class must be declared as public, if threr is no public class then we can use any name for the java program, if there is public class then the name of the class and the name of the file should be same .
eg.
```java
class A{
}
public class B{
}
class C{
}

//We can compile a java program , whenever we are compiling a java program for every class present in that program a seperate .class file will we generated.
//eg. 
//file name is Second.java

      
class A {
    public static void main(String[] args) {
        System.out.println("A class");
    }
}
class B {
    public static void main(String[] args) {
        System.out.println("B class");
    }
}
class C {
    public static void main(String[] args) {
        System.out.println("C class");
    }
}
class D{

}
```
---------------Compiling and Running ---------------------
```
 javac .\Second.java
 java A
  --> A class
 java C
  --> C class
 java D
  --> Error: Main method not found in class D, please define the main method as:
      public static void main(String[] args)                                 
      or a JavaFX application class must extend javafx.application.Application  
 java Second
  --> Error: Could not find or load main class Second    
      Caused by: java.lang.ClassNotFoundException: Second
```

if you are inside a package then execute in the below img terminal way.
![Screenshot (188)](https://github.com/16pravinkumar/JAVA_2024/assets/94048576/4df956d3-38a9-475c-980e-a9c548a6fdf5)


 # Import Statement Introduction 
 biggest advantages of using import is that we are not writing fully qualified name ie java.util.ArrayList a = new java.util.ArrayList() length of the code is reduced; 
 ```
      package Import_Statement_Introduction;
      public class Test {
      public static void main(String[] args) {
        java.util.ArrayList a = new java.util.ArrayList(); 
          }
      }
```

two types of import 
explicit import                            implicit import 
eg import java.util.ArrayList              eg import java.util.*
mostly in real world used explicit because it makes the code readiability

# Important points about Import Statement
there are two packages which are not have import statement they are both are bidefault present 
```
//1] java.lang  for String
//eg.
public class Test {
    public static void main(String[] args) {
        String s = new String();
        Thread t = new Thread();
        Exception e = new Exception();
    }
}
//it will not give any error because is present in java.lang packages

```
 2.  **default packages ie. curent working in same directory**
![image](https://github.com/16pravinkumar/JAVA_2024/assets/94048576/299da910-5600-45bc-9049-e39b254eeffe)
![image](https://github.com/16pravinkumar/JAVA_2024/assets/94048576/0b121109-7027-41a8-b9cd-52cb676bfcce)

here in Test.java we have not imported Execute.java package 


#Java source file structure-package statement
What is package in java?
A package is the encapsulation mechanism to group related classes and interfaces in a single unit. It helps in avoiding naming conflicts, improves code readability, and provides a mechanism for access control and security is also get improved. 


How to write a package and how to run ?
 ![image](https://github.com/16pravinkumar/JAVA_2024/assets/94048576/7c9856f4-5956-4098-bb3a-5cc796c9af36)


 # Important points about package Statement
  1. **inside a java file there is atmost one package is required.**
  2. **In a java file name there should be package at the top otherwise you will get an error.**
 ```
     eg
      import java.util.ArrayList;
      package com.Import_Statement_Introduction;
      public class Test {
          public static void main(String[] args) {
          System.out.println("Had");
          }
      }

```
o/p ===> error
- 3] flow order --> package then import statement then class|interface|enum


# class level modifiers: public and default
1. **Object Creation with Abstract Classes:**
   - If a class is abstract, we cannot create objects directly. Abstract classes are meant to be subclassed, and object instantiation is deferred to their concrete subclasses.

2. **Inheritance Restriction with Final Classes:**
   - If a class is marked as `final`, it prevents the creation of a child class. The `final` keyword indicates that the class cannot be extended or overridden.

#### Top-Level Classes (or Parent Classes):
   - For top-level classes, the following modifiers are allowed:
     - `public`
     - `default` (package-private)
     - `abstract`
     - `final`
     - `strictfp`

#### Low-Level Classes (or Child Classes):
   - For low-level classes (classes within other classes or subclasses), the following modifiers are allowed:
     - `public`
     - `default` (package-private)
     - `abstract`
     - `final`
     - `strictfp`
     - `private`
     - `protected`
     - `static`

# Java Class Modifiers and Visibility

In Java, class-level modifiers dictate the visibility and accessibility of classes. The two primary class-level modifiers are `public` and default (package-private). Here are examples for both:

### 1. Public Class

When a class is declared as `public`, it indicates that the class is accessible from any other class, irrespective of the package it belongs to.

**Example:**

```java
// File: com/example/myproject/PublicClassExample.java

package com.example.myproject;

public class PublicClassExample {
    public static void main(String[] args) {
        System.out.println("This is a public class.");
    }
}
```
In this example, `PublicClassExample` is declared as `public`. It can be accessed from any other class, even if it's in a different package.

![image](https://github.com/16pravinkumar/JAVA_2024/assets/94048576/a0b6fc92-a031-41c8-ad86-46cb62ccb8ec)
![image](https://github.com/16pravinkumar/JAVA_2024/assets/94048576/2c13ffde-c460-4bc6-9c45-9bd95a8b03b5)



### 2. Default (Package-Private) Class:
When no access modifier is specified (i.e., no public, private, or protected), the class has default (package-private) visibility. This means it is accessible only within the same package.

**Example:**

```java
Copy code
// File: com/example/myproject/DefaultClassExample.java

package com.example.myproject;

class DefaultClassExample {
    public static void main(String[] args) {
        System.out.println("This is a default class.");
    }
}
```
In this example, `DefaultClassExample` has default visibility because it lacks the `public` modifier. It is accessible only within the same package (`com.example.myproject`).


