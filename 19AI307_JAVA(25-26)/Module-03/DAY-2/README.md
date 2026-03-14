# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to perform the addition of two numbers using method overloading. The program should contain two overloaded methods named sum():

One that takes two integers and returns their sum.

One that takes two double values and returns their sum.

## AIM:
To write a Java program to perform the addition of two numbers using method overloading, where one overloaded method adds two integers and another adds two double values.

## ALGORITHM :
1. Start the program.
2. Create two sum() methods: one for integers and one for doubles.
3. Read two numbers from the user.
4. Check if the inputs are integers or doubles.
5. Call the correct sum() method based on the input type.
6. Display the result.
7. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class Addition {
    int sum(int a, int b) {
        return a + b;
    }
    double sum(double a, double b) {
        return a + b;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Addition add = new Addition();
        if (sc.hasNextInt()) {
            int a = sc.nextInt();
            int b = sc.nextInt();
            System.out.println(add.sum(a, b));
        } 
        else if (sc.hasNextDouble()) {
            double a = sc.nextDouble();
            double b = sc.nextDouble();
            System.out.println(add.sum(a, b));
        }
    }
}
```

## OUTPUT:

<img width="360" height="326" alt="image" src="https://github.com/user-attachments/assets/2122c7df-74aa-4ec5-acc3-eca9022e66d6" />


## RESULT:
Thus, the program successfully reads two values and performs addition using method overloading.



