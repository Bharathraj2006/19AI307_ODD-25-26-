# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## AIM:

To write a Java program to demonstrate handling of a NullPointerException.
## ALGORITHM :
1. Start the program.
2. Read an integer value from the user.
3. Assign null to the Integer object if the value is 0.
4. Attempt to convert the Integer object to a string using toString().
5. Handle the NullPointerException and display an appropriate message, then stop the program.



## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Bharath Raj P
RegisterNumber: 212223230031
*/
```

## SOURCE CODE:

```
import java.util.*;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        try{
            Integer a = sc.nextInt();
            if(a==0){
                a=null;
            }
            System.out.println(a.toString());
        }
        catch(NullPointerException e){
            System.out.println("Null Integer");
        }
    }
}
```





## OUTPUT:
<img width="483" height="234" alt="image" src="https://github.com/user-attachments/assets/1c1dcc92-5956-4598-8dd6-9b79453c5c08" />



## RESULT:
Hence, the Java program for demonstrating the handling of a NullPointerException was executed successfully and the appropriate message was displayed.
