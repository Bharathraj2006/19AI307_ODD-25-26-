# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.

<img width="505" height="363" alt="image" src="https://github.com/user-attachments/assets/f1440dc6-1556-42cf-a680-7f5557743179" />

## AIM:
To write a Java program to simulate an Air Traffic Control system for managing airplane landing requests.

## ALGORITHM :
1. Start the program.
2. Read the number of airplanes and runway status from the user.
3. Create an AirTrafficControl object with the given runway status.
4. Process each airplane's landing request based on runway availability.
5. Display whether each airplane is granted or denied landing and stop the program.




## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Bharath Raj P
RegisterNumber:  212223230031
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class AirTrafficControl {
    private boolean firstRequest;

    AirTrafficControl(boolean status) {
        firstRequest = status;
    }

    public void requestLanding(String airplaneName) {
        if (firstRequest) {
            System.out.println(airplaneName + " granted landing.");
            System.out.println(airplaneName + " landed successfully.");
        } else {
            System.out.println(airplaneName + " denied landing. Runway busy.");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        boolean status = sc.nextBoolean();
        sc.nextLine();

        AirTrafficControl atc = new AirTrafficControl(status);

        for (int i = 0; i < n; i++) {
            String airplaneName = sc.nextLine();

            if (status) {
                atc.requestLanding(airplaneName);
            } else {
                if (i == 0) {
                    System.out.println(airplaneName + " granted landing.");
                    System.out.println(airplaneName + " landed successfully.");
                } else {
                    System.out.println(airplaneName + " denied landing. Runway busy.");
                }
            }
        }
    }
}
```





## OUTPUT:
<img width="973" height="356" alt="image" src="https://github.com/user-attachments/assets/d56f6efd-7b24-41cc-8170-31cb01c96a06" />



## RESULT:
Hence, the Java program for simulating an Air Traffic Control system was executed successfully and the landing status of each airplane was displayed.
