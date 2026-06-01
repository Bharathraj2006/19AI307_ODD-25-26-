# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.


<img width="356" height="147" alt="image" src="https://github.com/user-attachments/assets/708b97d7-2b73-4b0a-9d45-f9a3f1b7c8dc" />

## AIM:
To write a Java program to set and display the name and priority of the current thread.

## ALGORITHM :
1. Start the program.
2. Read the thread name from the user.
3. Get the current thread using Thread.currentThread().
4. Set the thread name and priority.
5. Display the thread priority, name, and details, then stop the program.


## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
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

        Thread currentThread = Thread.currentThread();

        currentThread.setName(threadName);
        currentThread.setPriority(2);

        System.out.println("Priority of Thread: " + currentThread.getPriority());
        System.out.println("Name of Thread: " + currentThread.getName());
        System.out.println(currentThread);

        sc.close();
    }
}
```





## OUTPUT:


<img width="689" height="150" alt="image" src="https://github.com/user-attachments/assets/9a75ecdc-3393-4b1c-a426-7a5be317ff70" />


## RESULT:
Hence, the Java program for setting and displaying the name and priority of the current thread was executed successfully and the thread details were displayed.
