# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

## AIM:
To write a Java program that defines a class BankAccount with private attributes accountNumber and balance, and provides public getter and setter methods to access and modify these values.

## ALGORITHM :
1. Define a class BankAccount with two private instance variables:

        String accountNumber

        double balance

3. Create public getter and setter methods for both variables:

      getAccountNumber() and setAccountNumber()
   
   
      getBalance() and setBalance()

5. In the main() method, create a Scanner object to read input from the user.

6. Create an object of the BankAccount class.

7. Read the account number and balance from the user and store them using setter methods.

8. Retrieve and print the stored values using getter methods.

9. Close the Scanner and end the program.
    
## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:

```
import java.util.*;
class BankAccount {
    // Private instance variables
    private String accountNumber;
    private double balance;

    // Getter and Setter for accountNumber
    public String getAccountNumber() {
        return accountNumber;
    }
    public void setAccountNumber(String accountNumber) {
        this.accountNumber = accountNumber;
    }

    // Getter and Setter for balance
    public double getBalance() {
        return balance;
    }
    public void setBalance(double balance) {
        this.balance = balance;
    }
}

class prog{
    public static void main(String[] args){
        Scanner s = new Scanner(System.in);
        BankAccount b = new BankAccount();
        String accountNumber = s.nextLine();
        double balance = s.nextDouble();
        
        b.setAccountNumber(accountNumber);
        b.setBalance(balance);
        
        System.out.println("Account Number: "+b.getAccountNumber());
         //s.nextLine();
        System.out.println("Balance: "+b.getBalance());
    }
}
```

## OUTPUT:

<img width="805" height="391" alt="image" src="https://github.com/user-attachments/assets/747ae6e7-6249-424f-bcbe-cf4c9b6fbc7f" />

## RESULT:

Therfore the program successfully stores account details using setter methods and retrieves them using getter methods.


