# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to read a string from the user, compress it in memory using ByteArrayOutputStream + GZIPOutputStream, and then decompress it back using ByteArrayInputStream + GZIPInputStream.

<img width="972" height="233" alt="image" src="https://github.com/user-attachments/assets/f4b9077b-bc01-487b-8748-92d0a5563068" />

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
Program to implement a Serialization and Deserialization using Java
Developed by: Bharath Raj P
RegisterNumber:  212223230031
*/
```

## SOURCE CODE:
```

import java.io.*;
import java.util.Scanner;
import java.util.zip.GZIPOutputStream;
import java.util.zip.GZIPInputStream;

public class GZIPMemoryExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            String input = scanner.nextLine();

            ByteArrayOutputStream baos = new ByteArrayOutputStream();
            GZIPOutputStream gzipOut = new GZIPOutputStream(baos);
            gzipOut.write(input.getBytes("UTF-8"));
            gzipOut.close();

            byte[] compressedData = baos.toByteArray();
            System.out.println("Compressed data (bytes):");
            for (byte b : compressedData) {
                System.out.print(b + " ");
            }
            System.out.println("\nTotal bytes: " + compressedData.length);

            ByteArrayInputStream bais = new ByteArrayInputStream(compressedData);
            GZIPInputStream gzipIn = new GZIPInputStream(bais);
            InputStreamReader reader = new InputStreamReader(gzipIn, "UTF-8");
            BufferedReader br = new BufferedReader(reader);

            StringBuilder decompressed = new StringBuilder();
            String line;

            while ((line = br.readLine()) != null) {
                decompressed.append(line);
            }

            System.out.println("\nDecompressed string:");
            System.out.println(decompressed.toString());

        } catch (Exception e) {
            System.out.println("Error occurred.");
        }
    }
}
```






## OUTPUT:

<img width="1188" height="550" alt="image" src="https://github.com/user-attachments/assets/850f5387-b1cd-40d4-ada7-e870f57450ad" />


## RESULT:
Hence, the Java program for compressing and decompressing a string using GZIP streams was executed successfully and the compressed and decompressed outputs were displayed.
