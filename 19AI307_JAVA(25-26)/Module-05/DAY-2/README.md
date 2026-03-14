# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a program to demonstrate reading UTF strings using DataInputStream.

## AIM:
To write a Java program that reads a UTF string from the user, stores it in a file using DataOutputStream, and then reads the same UTF string back from the file using DataInputStream.

## ALGORITHM :
1. Start the program.
2. Create a file name to store the UTF data.
3. Read a string from the user using Scanner.
4. Create a DataOutputStream and write the UTF string to the file using writeUTF().
5. Create a DataInputStream and read the UTF string back from the file using readUTF().
6. Display the string that was read from the file.
7. End the program.

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.Scanner;

public class DataInputStreamUTFExample {
    public static void main(String[] args) {
        String fileName = "utfdata.dat";

        // write your code here
        try (Scanner scanner = new Scanner(System.in);
             DataOutputStream dout = new DataOutputStream(new FileOutputStream(fileName))) {
            
            // Read input from user
            String input = scanner.nextLine();
            
            // Write UTF string to file
            dout.writeUTF(input);
            
        } catch (IOException e) {
            System.out.println("Error writing to file: " + e.getMessage());
        }

        // Now read back the UTF string from the file
        try (DataInputStream din = new DataInputStream(new FileInputStream(fileName))) {
            String data = din.readUTF();
            System.out.println("String read from file: " + data);
        } catch (IOException e) {
            System.out.println("Error reading from file: " + e.getMessage());
        }
    }
}
```

## OUTPUT:

<img width="757" height="232" alt="image" src="https://github.com/user-attachments/assets/db85d7f4-3786-4c4e-8d0a-de7c16e367ec" />


## RESULT:
Thus, the program successfully reads a string from the user, writes it to a file (utfdata.dat), and then reads it back from the file using DataInputStream.


