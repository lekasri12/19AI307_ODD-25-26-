# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Define a class Car with brand (String), color (String), and year (int). Create 2 different objects of Car  Assign values to attributes. Print the details of both cars.import java.util.Scanner;

## AIM:
To define a class Car with attributes brand, color, and year; create two objects of the class; assign values to their attributes; and print the details of both cars.

## ALGORITHM :
1. Define a class Car with three data members:

     String brand
     String color
     int year
 and a method printDetails() to display these values.

3. In the main() method, create a Scanner object to read user inputs.

4. Create the first object car1 and read its brand, color, and year from the user.

5. Create the second object car2 and read its brand, color, and year.

6. Call printDetails() for car1 to display its information.

7. Call printDetails() for car2 to display its information.

7.Close the scanner and end the program.

## PROGRAM:

```
/*
Program to implement a Class and Objects using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class Car {
    String brand;
    String color;
    int year;

    void printDetails() {
        System.out.println("Brand: "+brand);
        System.out.println("Color: "+color);
        System.out.println("Year: "+year);
    }
}

class prog {
    public static void main(String[] args) {
        Scanner s = new Scanner (System.in);
        
        Car c1 = new Car();
        c1.brand = s.nextLine();
        c1.color=s.nextLine();
        c1.year=s.nextInt();
        c1.printDetails();
        s.nextLine();
        
        Car c2 = new Car();
        c2.brand = s.nextLine();
        c2.color=s.nextLine();
        c2.year=s.nextInt();
        c2.printDetails();
        s.nextLine();
        s.close();

    }
}
```

## OUTPUT:

<img width="502" height="618" alt="image" src="https://github.com/user-attachments/assets/14ca0191-49a3-4946-8130-f66f6e4b028c" />

## RESULT:

Therefore,the program successfully creates two Car objects and assigns values to their attributes.



