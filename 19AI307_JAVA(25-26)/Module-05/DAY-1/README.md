# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to convert a character stream to a byte stream using OutputStreamWriter.

<img width="964" height="142" alt="image" src="https://github.com/user-attachments/assets/5de50225-712c-4531-bf08-564502b60257" />

## AIM:
To write a Java program to write text into a file using OutputStreamWriter

## ALGORITHM :
1. Start the program.
2. Read the file name and content from the user.
3. Create a FileOutputStream for the specified file.
4. Write the content to the file using OutputStreamWriter.
5. Close the streams, display a success message, and stop the program.





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Bharath Raj P
RegisterNumber:  212223230031
*/
```

## SOURCE CODE:
```
import java.util.*;
import java.io.*;
public class Main{
    public static void main(String args[]) throws IOException{
        Scanner sc = new Scanner(System.in);
        String name = sc.next();
        String content = sc.next();
        byte[] c = content.getBytes();
        FileOutputStream f = new FileOutputStream(name);
        
        OutputStreamWriter o = new OutputStreamWriter(f);
        o.write(content);
        o.close();
        f.close();
        System.out.println("Text written successfully using OutputStreamWriter.");
        
    }
}
```






## OUTPUT:

<img width="1163" height="187" alt="image" src="https://github.com/user-attachments/assets/16f3d415-3564-41d1-80a6-1113619d9ed9" />


## RESULT:
Hence, the Java program for writing text into a file using OutputStreamWriter was executed successfully and the content was written to the file.
