# All about JAVA File Structure
A java program can contain any number of classes but atmost one class must be declared as public, if threr is no public class then we can use any name for the java program, if there is public class then the name of the class and the name of the file should be same .
eg.
class A{
}
public class B{
}
class C{
}

We can compile a java program , whenever we are compiling a java program for every class present in that program a seperate .class file will we generated.
eg. 
file name is Second.java

      
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
---------------Compiling and Running ---------------------
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

