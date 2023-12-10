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


if you are inside a package then execute in the below img terminal way.
![Screenshot (188)](https://github.com/16pravinkumar/JAVA_2024/assets/94048576/4df956d3-38a9-475c-980e-a9c548a6fdf5)


 # Import Statement Introduction 
 biggest advantages of using import is that we are not writing fully qualified name ie java.util.ArrayList a = new java.util.ArrayList() length of the code is reduced; 
      package Import_Statement_Introduction;
      public class Test {
      public static void main(String[] args) {
        java.util.ArrayList a = new java.util.ArrayList(); 
          }
      }


two types of import 
explicit import                            implicit import 
eg import java.util.ArrayList              eg import java.util.*
mostly in real world used explicit because it makes the code readiability

# Important points about Import Statement
there are two packages which are not have import statement they are both are bidefault present 
1] java.lang  for String
eg.
public class Test {
    public static void main(String[] args) {
        String s = new String();
        Thread t = new Thread();
        Exception e = new Exception();
    }
}
it will not give any error because is present in java.lang packages
2] default packages ie. curent working in same directory
![image](https://github.com/16pravinkumar/JAVA_2024/assets/94048576/299da910-5600-45bc-9049-e39b254eeffe)
![image](https://github.com/16pravinkumar/JAVA_2024/assets/94048576/0b121109-7027-41a8-b9cd-52cb676bfcce)

here in Test.java we have not imported Execute.java package 


