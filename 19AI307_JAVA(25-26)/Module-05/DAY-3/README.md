# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:

Read a file and reverse the order of words in each line.


<img width="494" height="275" alt="image" src="https://github.com/user-attachments/assets/10a547e0-4f7f-40b2-a76d-886ddc27b869" />

## AIM:
To write a Java program to compress and decompress a string using GZIP streams in memory.

## ALGORITHM :
1. Start the program.
2. Read a string from the user.
3. Compress the string using GZIPOutputStream and store it in a byte array.
4. Decompress the compressed data using GZIPInputStream.
5. Display the compressed bytes and decompressed string, then stop the program.



## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
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

        System.out.println("Reversed lines:");

        while (sc.hasNextLine()) {
            String line = sc.nextLine();

            if (line.equals("exit")) {
                break;
            }

            String[] words = line.split("\\s+");

            for (int i = words.length - 1; i >= 0; i--) {
                System.out.print(words[i]);
                if (i != 0) System.out.print(" ");
            }
            System.out.println();
        }

        sc.close();
    }
}

```






## OUTPUT:

<img width="839" height="283" alt="image" src="https://github.com/user-attachments/assets/9b07045b-d3b7-4b3d-9090-fc78710cac9f" />



## RESULT:
Hence, the Java program for compressing and decompressing a string using GZIP streams was executed successfully and the compressed and decompressed outputs were displayed.
