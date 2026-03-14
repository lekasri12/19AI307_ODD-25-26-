# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Create a program that reads a thread name and a priority (1–10), sets that priority to a new thread, prints both values.

## AIM:
To write a Java program that reads a thread name and a priority value (1–10) from the user, creates a new thread using the given name, sets the provided priority to that thread, and prints the thread name along with its priority.

## ALGORITHM :
1. Start the program.
2. Create a Scanner object to read input from the user.
3. Read the thread name as the first input line.
4. Read the priority (1–10) as the second input.
5. Create a custom thread class and assign the thread name using the constructor.
6. Create a new thread object using the input name.
7. Set the priority of the thread using setPriority().
8. Print the thread name and its assigned priority.
9. End the program.

## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: LEKASRI
RegisterNumber: 212223100025 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ThreadPriorityDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();
        int priority = sc.nextInt();

        Thread t = new Thread(() -> {});
        t.setName(threadName);
        t.setPriority(priority);

        System.out.println("Thread " + t.getName() + " priority is " + t.getPriority());

        sc.close();
    }
}
```

## OUTPUT:

<img width="757" height="296" alt="image" src="https://github.com/user-attachments/assets/633fde22-db3e-4656-a6ad-678ead6c0c30" />

## RESULT:
Thus, the program successfully reads a thread name and priority from the user, assigns the given priority to the new thread, and displays the result.



