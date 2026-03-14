# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Read a file and print only the lines containing the word "Java".

## AIM:
To write a Java program that reads multiple lines from the user and prints only those lines that contain the word "Java".

## ALGORITHM :
1. Start the program.
2. Create a Scanner object to read lines from the user.
3. Display a message indicating that lines containing the word "Java" will be printed.
4. Continuously read each line from the user.
5. If the user enters "exit", stop reading input.
6. Check if the current line contains the word "Java".
7. If yes, print that line.
8. Continue until "exit" is entered.
9. End the program.

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("Lines containing the word 'Java':");

        while (sc.hasNextLine()) {
            String line = sc.nextLine();

            if (line.equals("exit")) {
                break;
            }

            if (line.contains("Java")) {
                System.out.println(line);
            }
        }
    }
}
```

## OUTPUT:

<img width="498" height="160" alt="image" src="https://github.com/user-attachments/assets/3f365230-4226-4c35-81eb-90eb30f9839d" />


## RESULT:
Thus, the program successfully filters and prints only the lines that contain the word "Java".


