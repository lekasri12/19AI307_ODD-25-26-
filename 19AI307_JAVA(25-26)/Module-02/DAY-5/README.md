# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:

Create a class Employee with method display(). Inside display(), return the current object using this. Create another method that calls display().printName()

## AIM:

To create an Employee class where the display() method returns the current object using this, and demonstrate calling display().printName() from another method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an Employee class with variables and methods.
4.	In the main method, create a Scanner object to read input.
5.	Create an object of the Employee class.
6.	Read the employee name from the user.
7.	Call the setName() method to store the name using this keyword.
8.	Call the display() method, which returns the current object using this.
9.	Chain the returned object with printName() to display the employee’s name.
10.	Close the Scanner.
11.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class Employee {
    String name;
    void setName(String name) {
        // assign name using this
        this.name = name;
    }
    Employee display() {
        // return the current object using this
        return this;
    }

    void printName() {
        // Print name
        System.out.println("Employee Name: " + name);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Employee emp = new Employee();
        String empName = sc.nextLine();
        emp.setName(empName);

        // Call display() and chain with printName()
        emp.display().printName();

        sc.close();
    }
}
```

## OUTPUT:

<img width="622" height="238" alt="image" src="https://github.com/user-attachments/assets/dc3dbe7b-f92f-45f7-ab64-4857b8ec2f55" />

## RESULT:

Therefore the program successfully returns the current object using this inside the display() method.



