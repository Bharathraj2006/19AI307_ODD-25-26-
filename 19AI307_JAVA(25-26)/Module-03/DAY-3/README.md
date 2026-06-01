# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class GameScore with method finalScore().
```
Subclasses:
ArcadeGame: score = baseScore + (level × 100)
PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500
```

## AIM:
To write a Java program to demonstrate abstraction by calculating the final score of different game types using abstract classes.

## ALGORITHM :
1. Start the program.
2. Create an abstract class GameScore with an abstract method finalScore().
3. Read the game type and required input values from the user.
4. Create an object of the corresponding game class (Agame or Pgame).
5. Calculate and display the final score, then stop the program.




## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Bharath Raj P
RegisterNumber:  212223230031
*/
```

## SOURCE CODE:

```
import java.util.*;
abstract class GameScore{
    abstract int finalScore();
}
class Agame extends GameScore{
    private int bs;
    private int level;
    Agame(int bs,int level){
        this.bs = bs;
        this.level=level;
    }
    int finalScore(){
        return bs+(level*100);
    }
}
class Pgame extends GameScore{
    private int attempts;
    Pgame(int attempts){
        this.attempts = attempts;
    }
    int finalScore(){
        if (attempts<=3){
            return 1000-(attempts*100);
        }
        else{
            return 500;
        }
        
    }
}
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        

        GameScore g;
        if(type==1){
            int bs = sc.nextInt();
            int level = sc.nextInt();
            g = new Agame(bs,level);
        }
        else{
            int attempts = sc.nextInt();
            g = new Pgame(attempts);
        }
        System.out.println(g.finalScore());
    }
}
```





## OUTPUT:

<img width="330" height="149" alt="image" src="https://github.com/user-attachments/assets/db87d32c-326f-4fc9-80e7-381ad2d01afb" />


## RESULT:
Hence, the Java program for demonstrating abstraction using abstract classes was executed successfully and the final score was displayed.
