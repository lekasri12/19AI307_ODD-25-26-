# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

## AIM:
To write a Java program that defines a method cube(int x) which internally calls the method square(int x) to compute the cube of a number.

## ALGORITHM :
1. Define a class demo with two methods:

     square(int n) → returns n * n.
     cube(int n) → returns n * square(n) by calling the square() method internally.

2. In the main class, read an integer input from the user.

3. Create an object of the demo class.

4. Call the cube() method using the object and print the result.

5. End the program.

## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class prog{
    static int square(int x){
        return x*x;
    }
    static int cube(int x){
        return x*(square(x));
    }
}
public class Main{
    public static void main(String[] args){
        Scanner s = new Scanner(System.in);
        prog p = new prog();
        int x = s.nextInt();
        System.out.println(p.cube(x));
    }
}
```

## OUTPUT:

<img width="340" height="177" alt="image" src="https://github.com/user-attachments/assets/7885966c-e554-4745-a825-077e54e807e7" />

## RESULT:

Therefore the program successfully computes the cube of a number by internally using the square method.


