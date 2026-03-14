# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an inner class and access it from the outer class.

## AIM:
To demonstrate accessing an inner class from an outer class in Java.

## ALGORITHM :
1.	Create an outer class with a private variable.
2.	Define an inner class inside it with a method to access the outer variable.
3.	In main(), create an object of the outer class.
4.	Use it to create an object of the inner class.
5.	Call the inner class method.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class OuterClass {
    String name;
    OuterClass(String name) {
        this.name = name;
    }
    void display() {
        InnerClass inner = new InnerClass();
        inner.showMessage();
    }
    class InnerClass {
        void showMessage() {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("");
        String input = scanner.next();
        scanner.close();
        OuterClass outer = new OuterClass(input);
        outer.display();
    }
}
```

## OUTPUT:

<img width="848" height="185" alt="image" src="https://github.com/user-attachments/assets/14b79766-dab2-44db-9dde-0f4fd5b97b42" />


## RESULT:
Thus, the program successfully accesses and prints data from the inner class using the outer class.


