# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
Given a month number (1 to 12), print which quarter of the year it belongs to:
Months 1,2,3 → "First Quarter"
Months 4,5,6 → "Second Quarter"
Months 7,8,9 → "Third Quarter"
Months 10,11,12 → "Fourth Quarter"
If the number is not in 1-12, print "Invalid Month".

## AIM:
To write a java program to get the month from user and and display appropriate output for the given input.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the month number from the user.
4.	Check if the month is between 1 and 3.If yes, print "First Quarter".
5.	Else check if the month is between 4 and 6 → print "Second Quarter".
6.	Else check if the month is between 7 and 9 or 10 and 12 → print "Third" or "Fourth Quarter" accordingly.
7.	If the month is not between 1–12 → print "Invalid Month".
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
public class MonthQuarter {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int month = sc.nextInt();
        if (month >= 1 && month <= 3) {
            System.out.println("First Quarter");
        } else if (month >= 4 && month <= 6) {
            System.out.println("Second Quarter");
        } else if (month >= 7 && month <= 9) {
            System.out.println("Third Quarter");
        } else if (month >= 10 && month <= 12) {
            System.out.println("Fourth Quarter");
        } else {
            System.out.println("Invalid Month");
        }
    }
}
```

## OUTPUT:

<img width="462" height="178" alt="image" src="https://github.com/user-attachments/assets/b8cfbc3f-bf30-4a7f-aba1-8e2896dac427" />

## RESULT:

Thus , the java program to get the month from user and and display appropriate output for the given input 
was successfully executed .



