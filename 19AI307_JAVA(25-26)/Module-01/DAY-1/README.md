# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is preparing a countdown for her rocket launch game. She has a starting number and wants to understand how subtracting with -- works in Java. But she's puzzled by the two types: Post-decrement (a--) → value is used first, then decreased Pre-decrement (--a) → value is decreased first, then used To complete the launch program, help Lovely: Take a countdown number as input. Apply both post-decrement and pre-decrement on it. Show how the value changes in each case.

## AIM:
To write a Java program that accepts an integer input and demonstrates the difference between post-decrement (a--) and pre-decrement (--a) operators.

## ALGORITHM :
1.	Initialize the program and the Scanner class.
2. Read an integer from the user and store it in variable a.
3. Print the initial value of a.
4. Print the value of a (before change), decrement it, then print the updated a.
5. Decrement a first, then print the new value and the final a.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## Sourcecode.java:

```
import java.util.Scanner;
public class main{
    public static void main(String[] args){
        Scanner s = new Scanner(System.in);
        int a = s.nextInt();
        System.out.println("Initial countdown = "+a);
        int post = a--;
        System.out.println("After post-decrement (a--) = "+post+", Now a = "+a);
        int pre = --a;
        System.out.println("After pre-decrement (--a) = "+pre+", Now a = "+a);
    }
}
```

## OUTPUT:

<img width="997" height="296" alt="image" src="https://github.com/user-attachments/assets/32e13cbb-c46d-48ec-b9ed-5a6e9fc1ff95" />

## RESULT:

Thus, the Java program that does post-decrement and pre-decrement operators are executed successfully.




