# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a Java class with a constructor that accepts two numbers as input parameters. The constructor should calculate and display the sum, difference, product, and quotient of the two numbers.

<img width="416" height="179" alt="image" src="https://github.com/user-attachments/assets/514d96f7-e1c2-4f5e-8ffe-44649182bb01" />

## AIM:
To write a Java program to perform basic arithmetic operations using a constructor.

## ALGORITHM :
1. Start the program.
2. Read two numbers `a` and `b` from the user.
3. Create an object of the `calculation` class and pass `a` and `b` to the constructor.
4. Calculate the sum, difference, product, and quotient of the two numbers inside the constructor.
5. Display the results and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Bharath Raj P
RegisterNumber:  212223230031
*/
```

## SOURCE CODE:

```
import java.util.*;
public class calculation{
    public calculation(double a,double b){
       double sum = a+b;
       double sub = a-b;
       double mul = a*b;
       double quot = a/b;
       
       System.out.println("Sum: "+sum);
       System.out.println("Difference: "+sub);
       System.out.println("Product: "+mul);
       System.out.println("Quotient: "+quot);
    }
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        double a =sc.nextInt();
        sc.nextLine();
        double b = sc.nextInt();
        calculation o = new calculation(a,b);
}
}

```


## OUTPUT:
<img width="714" height="403" alt="image" src="https://github.com/user-attachments/assets/012eb8ce-cbc4-434c-b2c0-f93bcf04b758" />



## RESULT:
Hence, the Java program for performing basic arithmetic operations using a constructor was executed successfully and the results were displayed.
