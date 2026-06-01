# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.
The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.
Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.
```
Hidden Clue:
Use Singleton to manage shared access.
Count and log each print job submission.
Validate that state is preserved across all accesses.
```
## AIM:


## ALGORITHM :
1. Start the program.
2. Create a Singleton class PrintSpoolerManager with a single shared instance.
3. Read the number of print job requests from the user.
4. For each request, access the Singleton instance and submit a print job.
5. Display the department name and total jobs in the queue, then stop the program.


## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Bharath Raj P
RegisterNumber:  212223230031
*/
```

## SOURCE CODE:
```
import java.util.*;

class PrintSpoolerManager {
    private static PrintSpoolerManager instance;
    private int ac =0;
    public static PrintSpoolerManager getInstance() {
        if(instance==null){
            instance = new PrintSpoolerManager();
        }
        return instance;
    }

    public int submitJob() {
      ac++;
      return ac;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String dept = sc.nextLine();
            PrintSpoolerManager spooler = PrintSpoolerManager.getInstance();
            int total = spooler.submitJob();
            System.out.println(dept + " submitted a print job. Total Jobs in Queue: " + total);
        }
    }
}
```






## OUTPUT:

<img width="1173" height="352" alt="image" src="https://github.com/user-attachments/assets/62d9ec51-b1ba-4bab-9ed2-cc960bbf864e" />


## RESULT:
Hence, the Java program for demonstrating the Singleton Design Pattern using a Print Spooler Manager was executed successfully and the print job details were displayed.
