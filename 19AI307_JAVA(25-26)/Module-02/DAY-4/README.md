# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:

Create a constructor in a class and call a normal method from it. 

## AIM:

To write a Java program to create a constructor in a class and call a normal method from it. 

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the student’s name from the user.
4.	Read the student’s marks from the user.
5.	Create a student object by passing the name and marks to the constructor.
6.	Inside the constructor, store the name and marks, then call the displayRes() method.
7.	In the displayRes() method, print the student’s name and marks.
8.	Check if marks are less than 35:
	
  • If yes, print “Fail”. Otherwise, print “Pass”.

10. End the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:

```
import java.util.*;
class student{
    String name;
    int marks;
    
    public student(String name,int marks){
        this.name=name;
        this.marks=marks;
        displayRes();
    }
    
    public void displayRes(){
        System.out.println("Student Name: "+name);
        System.out.println("Marks Scored: "+marks);
        if(marks <35){
            System.out.println("Status: Fail");
        }
        else {
            System.out.println("Status: Pass");
        }
    }
}

public class prog{
    public static void main(String[] args){
        Scanner s = new Scanner(System.in);
        String name = s.nextLine();
        int marks = s.nextInt();
        student t = new student(name,marks);
    }
}
```

## OUTPUT:

<img width="562" height="381" alt="image" src="https://github.com/user-attachments/assets/50d0208b-352f-4a08-8c99-0ae9c228e2f8" />

## RESULT:

Therefore the program successfully creates a constructor in a class and call a normal method from it. 




