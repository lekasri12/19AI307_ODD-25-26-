# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.

Note : Read the threadname from the User

## AIM:
To read a thread name from the user and display the current thread’s name and priority.

## ALGORITHM :
1.	Read the thread name from the user.
2.	Get the reference of the current thread using Thread.currentThread().
3.	Set the name of the current thread using setName().
4.	Retrieve the thread’s name and priority using getName() and getPriority().
5.	Display both values.

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class ThreadDetails {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        // Read thread name from user
        String threadName = sc.nextLine();
        // Get reference to current thread
        Thread currentThread = Thread.currentThread();
        // Set the thread's name
        currentThread.setName(threadName);
        // Display thread information
        System.out.println("Priority of Thread: " + currentThread.getPriority());
        System.out.println("Name of Thread: " + currentThread.getName());
        System.out.println(currentThread);
    }
}
```

## OUTPUT:

<img width="697" height="201" alt="image" src="https://github.com/user-attachments/assets/206d6347-d0a3-4344-bc60-372c42bc15b1" />

## RESULT:
Thus, the program successfully reads the thread name from the user and displays the current thread’s name and priority.


