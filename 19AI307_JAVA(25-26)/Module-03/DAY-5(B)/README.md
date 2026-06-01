# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to find the square root of a number using Double wrapper class.

<img width="340" height="122" alt="image" src="https://github.com/user-attachments/assets/3470347e-2bb5-4870-9f7b-4b5576be4b34" />

## AIM:
To write a Java program to find the square root of a given number.

## ALGORITHM :
1. Start the program.
2. Read a number from the user.
3. Calculate the square root of the number using Math.sqrt().
4. Store the result in a variable.
5. Display the square root and stop the program.




## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Bharath Raj P
RegisterNumber:  212223230031
*/
```

## SOURCE CODE:
```
import java.util.*;
public class SquareRoot{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        double number = sc.nextDouble();
        Double sqrt = Math.sqrt(number);
        System.out.println("Square root of "+ number +" is: "+sqrt);
    }
}
```






## OUTPUT:

<img width="721" height="181" alt="image" src="https://github.com/user-attachments/assets/48f65f8e-8f2f-4d03-99be-9ed2e79a6a55" />


## RESULT:
Hence, the Java program for finding the square root of a given number was executed successfully and the result was displayed.
