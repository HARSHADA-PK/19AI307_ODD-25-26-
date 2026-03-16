# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)

For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

## AIM:
To develop a Java program that calculates the final gold purchase amount for different customer types using inheritance.  
The program should apply:
- **2% discount** for RegularCustomer  
- **5% discount + 1% cashback** for PremiumCustomer  
and compute the final payable amount based on purchase weight and gold rate per gram.

## ALGORITHM :
1. Create a base class **Customer** with attributes:
   - `customerId`
   - `name`
   - `purchaseWeight`
   - `goldRatePerGram`
2. Implement a constructor to initialize the above values.
3. Create a method `getDiscountRate()` that returns `0` in the base class.
4. Create a method `calculateFinalPrice()`:
   - Calculate discount amount  
   - Subtract discount from gold rate  
   - Multiply effective rate with purchase weight  
5. Create a `display()` method to print customer details.
6. Create **RegularCustomer** class extending Customer:
   - Override `getDiscountRate()` to return **2%**
   - Override `display()` to show details
7. Create **PremiumCustomer** class extending Customer:
   - Override `getDiscountRate()` to return **5%**
   - Add `getCashback()` returning **1% of final price**
   - Override `display()` to show details including cashback
8. In the `main()` method:
   - Read user input (type, id, name, weight, gold rate)
   - Based on type, create the appropriate customer object  
   - Call `display()` to print output
9. End the program.

## PROGRAM:
  ```
/*
Program to implement a conditional statement using Java
Developed by: Harshada P K
RegisterNumber:  212224060097
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    int getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100.0;
        return purchaseWeight * (goldRatePerGram - discountAmount);
    }

    void display(String type) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: " + type);
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    int getDiscountRate() {
        return 2;
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    int getDiscountRate() {
        return 5;
    }

    double calculateCashback() {
        return calculateFinalPrice() * 0.01;
    }

    void display(String type) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: " + type);
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(calculateCashback()));
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String customerType = sc.nextLine().trim(); 
        String customerId = sc.nextLine();
        String name = sc.nextLine();
        double purchaseWeight = Double.parseDouble(sc.nextLine());
        double goldRate = Double.parseDouble(sc.nextLine());

        if (customerType.equalsIgnoreCase("Premium")) {
            PremiumCustomer p = new PremiumCustomer(customerId, name, purchaseWeight, goldRate);
            p.display("Premium"); 
        } else if (customerType.equalsIgnoreCase("Regular")) {
            RegularCustomer r = new RegularCustomer(customerId, name, purchaseWeight, goldRate);
            r.display("Regular");
        } else {
            Customer c = new Customer(customerId, name, purchaseWeight, goldRate);
            c.display("Standard");
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="832" height="701" alt="image" src="https://github.com/user-attachments/assets/80fdf85b-2b42-4187-a689-ee5603a70f52" />

## RESULT:
The program successfully computes the final gold purchase price for:
- General customers  
- Regular customers (with 2% discount)  
- Premium customers (with 5% discount and 1% cashback)

It displays complete details including customer type, discount applied, final price, and cashback for premium customers.

