# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:
finalPrice = purchaseWeight * (goldRatePerGram - discount)
For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

## AIM:

To write a Java program to demonstrate inheritance and method overriding for calculating gold purchase discounts and cashback for different customer types.
## ALGORITHM :
1. Start the program.
2. Create a base class Customer and derived classes RegularCustomer and PremiumCustomer.
3. Read customer details such as type, ID, name, purchase weight, and gold rate.
4. Calculate the final price based on the discount applicable to the customer type.
5. Display the customer details, discount, final price, and cashback (for Premium customers) and stop the program.




## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: 
RegisterNumber:  
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

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        String discountStr = getDiscountRate() % 1 == 0 ? String.valueOf((int)getDiscountRate()) : String.valueOf(getDiscountRate());

        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + discountStr + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 2;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        String discountStr = getDiscountRate() % 1 == 0 ? String.valueOf((int)getDiscountRate()) : String.valueOf(getDiscountRate());

        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + discountStr + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 5;
    }

    double getCashback() {
        return calculateFinalPrice() * 0.01;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        String discountStr = getDiscountRate() % 1 == 0 ? String.valueOf((int)getDiscountRate()) : String.valueOf(getDiscountRate());

        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + discountStr + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
        System.out.println("Cashback: " + df.format(getCashback()));
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        for (int i = 0; i < 3 && sc.hasNext(); i++) {
            String type = sc.nextLine().trim();
            String id = sc.nextLine().trim();
            String name = sc.nextLine().trim();
            double weight = Double.parseDouble(sc.nextLine().trim());
            double goldRate = Double.parseDouble(sc.nextLine().trim());

            Customer c;
            if (type.equalsIgnoreCase("Regular")) {
                c = new RegularCustomer(id, name, weight, goldRate);
            } else {
                c = new PremiumCustomer(id, name, weight, goldRate);
            }

            c.display();
        }

        sc.close();
    }
}
```
## OUTPUT:

<img width="795" height="452" alt="image" src="https://github.com/user-attachments/assets/47513f14-bf97-443b-82c5-c6e0b07ec078" />


## RESULT:
Hence, the Java program for demonstrating inheritance and method overriding in a gold purchase management system was executed successfully and the customer details, discounts, final price, and cashback were displayed.
