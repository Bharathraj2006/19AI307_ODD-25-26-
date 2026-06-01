# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Create a program that reads a thread name and a priority (1–10), sets that priority to a new thread, prints both values.

## AIM:
To write a Java program to create a thread and set its name and priority.

## ALGORITHM :
1. Start the program.
2. Read the thread name and priority from the user.
3. Create a new Thread object.
4. Set the thread name and priority using setter methods.
5. Display the thread name and priority, then stop the program.




## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Bharath Raj P
RegisterNumber:  212223230031
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();
        int priority = sc.nextInt();

        Thread t = new Thread();
        t.setName(threadName);
        t.setPriority(priority);

        System.out.println("Thread " + t.getName() +
                           " priority is " + t.getPriority());
    }
}
```






## OUTPUT:


<img width="747" height="251" alt="image" src="https://github.com/user-attachments/assets/51aa5781-2b2d-4f46-9339-bc4a4c1a7293" />


## RESULT:
Hence, the Java program for creating a thread and setting its name and priority was executed successfully and the thread details were displayed.
