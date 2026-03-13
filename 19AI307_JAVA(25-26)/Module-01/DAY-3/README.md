# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

Print Multiplication Table of a Number

## AIM:

To write a Java program that reads a number from the user and prints its multiplication table from 1 to 10 using looping statements.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read input from the user.
4.	Read an integer value.
5.	Use a for loop that runs from 1 to 10.
6.	In each iteration, multiply the given number by the loop variable.
7.	Print the result in the format: num x i = product
8.	End the loop.
9.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
public class Main{
    public static void main(String[] args){
        Scanner s = new Scanner(System.in);
        int n = s.nextInt();
        for ( int i = 1 ; i<=10;i++){
            System.out.println(n+" x "+i+" = "+n*i);
        }
    }
}
```

## OUTPUT:

<img width="410" height="648" alt="image" src="https://github.com/user-attachments/assets/d863a3de-73a6-49a8-b17d-013e313ec5db" />

## RESULT:

Thus, the Java program to print the multiplication table of a number using looping statements was successfully written, executed, and verified.



