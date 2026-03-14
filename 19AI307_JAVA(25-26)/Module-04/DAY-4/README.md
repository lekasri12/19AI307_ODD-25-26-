# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create a program that sends different types of notifications: "email", "sms", and "push". Use the Factory Pattern to generate the appropriate notification sender and call its notifyUser() method.

## AIM:
To implement the Factory Design Pattern to send different types of notifications — Email, SMS, and Push.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Notification interface with the method notifyUser().
4.	Implement this interface in classes EmailNotification, SMSNotification, and PushNotification.
5.	Create a NotificationFactory class to generate objects based on input type.
6.	In main(), read the notification type and get the corresponding object from the factory.
7.	Call the notifyUser() method to send the notification.


## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: LEKASRI G
RegisterNumber:  212223100025
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
interface Notification {
    void notifyUser();
}
class EmailNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Email Notification");
    }
}

class SMSNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending SMS Notification");
    }
}

class PushNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Push Notification");
    }
}
class NotificationFactory {
    public Notification createNotification(String type) {
        if (type == null) return null;
        switch(type.toLowerCase()) {
            case "email":
                return new EmailNotification();
            case "sms":
                return new SMSNotification();
            case "push":
                return new PushNotification();
            default:
                return null;
        }
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        NotificationFactory factory = new NotificationFactory();
        
        while (true) {
            String input = sc.nextLine();
            if (input.equalsIgnoreCase("exit")) break;
            
            Notification n = factory.createNotification(input);
            if (n != null) n.notifyUser();
            else System.out.println("Invalid notification type: " + input);
        }
        
        sc.close();
    }
}
```

## OUTPUT:

<img width="682" height="305" alt="image" src="https://github.com/user-attachments/assets/7d760ec0-ae93-4320-a45d-268c107f10f7" />

## RESULT:

Thus, the program successfully creates and sends the appropriate type of notification using the Factory Pattern.


