# Ex.No:3(F) WRAPPER CLASS

## QUESTION:

Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## AIM:
 To write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number and store its digit count.
4.	Set sum = 0.
5.	Repeat while number > 0: take last digit.
6.	Raise digit to power of digits and add to sum.
7.	Remove last digit from number.
8.	If sum equals original number → Armstrong, else not.


## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int original = num;
        String numStr = Integer.toString(num);
        int digits = numStr.length();
        int sum = 0;
        while (num > 0) {
            int digit = num % 10;
            sum += Math.pow(digit, digits); 
            num /= 10;
        }
        if (sum == original) {
            System.out.println(original + " is an Armstrong number.");
        } else {
            System.out.println(original + " is not an Armstrong number.");
        }
    }
}
```

## OUTPUT:

<img width="785" height="252" alt="image" src="https://github.com/user-attachments/assets/345bcada-8c94-4d73-948b-eb55515ecbc1" />

## RESULT:

Thus, the program successfully checks whether the given number is an Armstrong number or not.

