# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.

```
Bot Types:
SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".
RainBot: Predicts "COLD" if temperature < 20, else "WARM".
```
## AIM:
To write a Java program to demonstrate interfaces by predicting weather conditions using different weather bots.

## ALGORITHM :
1. Start the program.
2. Create an interface WeatherBot with the method predict().
3. Read the temperature and bot type from the user.
4. Create an object of SunBot or RainBot based on the bot type.
5. Predict and display the weather condition, then stop the program.




## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Bharath Raj P
RegisterNumber:  212223230031
*/
```

## SOURCE CODE:
```
import java.util.*;
interface WeatherBot{
    String predict(int temperature);
}
class SunBot implements WeatherBot{
    public String predict(int temperature){
        if(temperature>30){
            return "HOT";
        }
        else{
            return "MODERATE";
        }
    }
}

class RainBot implements WeatherBot{
    public String predict(int temperature){
        if(temperature<20){
            return "COLD";
        }
        else{
            return "WARM";
        }
    }
}
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int temp = sc.nextInt();
        int botType = sc.nextInt();
        WeatherBot bot;
        if(botType==1){
            bot = new SunBot();
        }
        else{
            bot = new RainBot();
        }
        System.out.println(bot.predict(temp));
    }
}

```






## OUTPUT:
<img width="321" height="109" alt="image" src="https://github.com/user-attachments/assets/1fcd212c-a88f-4eb6-b980-15e7a744fd42" />



## RESULT:
Hence, the Java program for demonstrating interfaces and weather prediction was executed successfully and the corresponding weather condition was displayed.
