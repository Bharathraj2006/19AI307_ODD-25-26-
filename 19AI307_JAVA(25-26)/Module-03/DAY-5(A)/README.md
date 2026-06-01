# Ex.No:3(E) INNER CLASS

## QUESTION:

Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.
<img width="326" height="117" alt="image" src="https://github.com/user-attachments/assets/c6eb157b-1a41-4da1-b482-5d198ac40cc3" />

## AIM:
To write a Java program to check whether a given number is an Armstrong number.

## ALGORITHM :
1. Start the program.
2. Read an integer number from the user.
3. Find the number of digits in the given number.
4. Calculate the sum of each digit raised to the power of the number of digits.
5. Compare the calculated sum with the original number and display whether it is an Armstrong number, then stop the program.



## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Bharath Raj P
RegisterNumber:  212223230031
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        int temp=num,sum=0;
        int digits = Integer.toString(num).length();
        while(temp>0){
            int d = temp%10;
            sum+=Math.pow(d,digits);
            temp/=10;
        }
        if(sum==num){
            System.out.println(num+" is an Armstrong number.");
        }
        else{
            System.out.println(num+" is not an Armstrong number.");
        }
    }
}

```






## OUTPUT:

<img width="757" height="198" alt="image" src="https://github.com/user-attachments/assets/e19aa0d0-a576-4120-a6b3-8531a3a0d9e0" />


## RESULT:
Hence, the Java program for checking whether a given number is an Armstrong number was executed successfully and the result was displayed.
