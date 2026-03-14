# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)

For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

## AIM:
To write a Java program using inheritance to calculate the final gold price for different types of customers (Regular and Premium) based on discounts and cashback.

## ALGORITHM :
1.	Define a base class Customer with attributes customerId, name, and purchaseWeight.
2.	Define RegularCustomer subclass with a 2% discount on the gold rate.
3.	Define PremiumCustomer subclass with a 5% discount and 1% cashback on the final price.
4.	Input the base gold rate per gram at runtime.
5.	For each customer, calculate and display the final price (and cashback for premium).

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:
```
import java.util.*;
import java.text.*;
class Customer 
{
    String customerId, name;
    double purchaseWeight, goldRatePerGram;
    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) 
    {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }
    int getDiscountRate() 
    {
        return 0;
    }
    double calculateFinalPrice() 
    {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }
    void display() 
    {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer 
{
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) 
    {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }
    int getDiscountRate() 
    {
        return 2; 
    }
    void display() 
    {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer 
{
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) 
    {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }
    int getDiscountRate() 
    {
        return 5; 
    }
    double calculateCashback() 
    {
        return calculateFinalPrice() * 0.01; 
    }
    void display() 
    {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(calculateCashback()));
    }
}

public class prog 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        String type = sc.next();          
        String id = sc.next();
        String name = sc.next();
        double weight = sc.nextDouble();
        double rate = sc.nextDouble();
        Customer c;
        if (type.equalsIgnoreCase("Regular")) 
        {
            c = new RegularCustomer(id, name, weight, rate);
        } 
        else 
        {
            c = new PremiumCustomer(id, name, weight, rate);
        }
        c.display();
        sc.close();
    }
}
```

## OUTPUT:

<img width="823" height="705" alt="image" src="https://github.com/user-attachments/assets/36f2a9e8-c059-4fa1-8840-d062ac7dfd7c" />


## RESULT:
Thus, the program successfully calculates and displays the final payable price for both Regular and Premium customers with applicable discounts and cashback.



