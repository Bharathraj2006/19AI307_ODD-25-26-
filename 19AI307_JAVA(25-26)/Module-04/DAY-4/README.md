# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Simulate a fan speed controller using the State Pattern. Each time the user types "next", change fan speed from Off -> Low -> Medium -> High -> Off.

<img width="207" height="121" alt="image" src="https://github.com/user-attachments/assets/9deed9ab-83c3-40fb-b417-539f1b32a4a3" />

## AIM:
To write a Java program to demonstrate the State Design Pattern for controlling fan speed states.

## ALGORITHM :
1. Start the program.
2. Create different state classes representing Off, Low, Medium, and High fan speeds.
3. Initialize the fan in the Off state.
4. Read user commands and change the fan state when "next" is entered.
5. Display the current fan state after each transition and stop when "exit" is entered.




## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface State {
    void next(Fan fan);
    String toString();
}

class Off implements State {
    public void next(Fan fan) {
        fan.setState(new Low());
        System.out.println("Fan is on Low");
    }
    public String toString() {
        return "Off";
    }
}

class Low implements State {
    public void next(Fan fan) {
        fan.setState(new Medium());
        System.out.println("Fan is on Medium");
    }
    public String toString() {
        return "Low";
    }
}

class Medium implements State {
    public void next(Fan fan) {
        fan.setState(new High());
        System.out.println("Fan is on High");
    }
    public String toString() {
        return "Medium";
    }
}

class High implements State {
    public void next(Fan fan) {
        fan.setState(new Off());
        System.out.println("Fan is Off");
    }
    public String toString() {
        return "High";
    }
}

class Fan {
    private State state;
    
    public Fan() {
        state = new Off();
    }
    
    public void setState(State state) {
        this.state = state;
    }
    
    public void next() {
        state.next(this);
    }
    
    public String getState() {
        return state.toString();
    }
}

public class FanController {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Fan fan = new Fan();
        
        while (true) {
            String input = scanner.nextLine().trim().toLowerCase();
            if (input.equals("next")) {
                fan.next();
            } else if (input.equals("exit")) {
                break;
            }
        }
        scanner.close();
    }
}

```






## OUTPUT:

<img width="489" height="331" alt="image" src="https://github.com/user-attachments/assets/60082085-eaa3-45fc-83f0-15bd442cab05" />


## RESULT:
Hence, the Java program for demonstrating the State Design Pattern in a fan controller was executed successfully and the fan states were changed and displayed accordingly.
