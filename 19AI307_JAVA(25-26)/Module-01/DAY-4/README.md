# Ex.No:1(D) ARRAYS

## QUESTION:

Write a Java program to print all elements in an array that are greater than a given value


## AIM:

To write a Java program that prints all elements in an array greater than a given value.

## ALGORITHM :

1. Start the program and create a Scanner object.
2. Read the size n and elements of the array.
3. Read a value to compare with.
4. Use a loop to check and print elements greater than the given value.
5. End the program.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
public class GreaterThanValue {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        int value = sc.nextInt();
        boolean found = false;
        for (int i = 0; i < n; i++) {
            if (arr[i] > value) {
                System.out.println(arr[i]);
                found = true;
            }
        }
        if (!found) {
            System.out.println("No elements greater than " + value);
        }
    }
}
```

## OUTPUT:

<img width="685" height="616" alt="image" src="https://github.com/user-attachments/assets/94a26158-a18d-4d88-a67e-4797fe264061" />

## RESULT:

Thus,the program successfully prints all array elements greater than the given value.




