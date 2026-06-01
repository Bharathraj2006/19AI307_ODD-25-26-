# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Employee with method display(). Inside display(), return the current object using this. Create another method that calls display().printName()
 
<img width="286" height="104" alt="image" src="https://github.com/user-attachments/assets/ea1351eb-c140-4939-b752-8bf5801d2591" />

## AIM:
To write a Java program to demonstrate the use of the this keyword by returning the current object and displaying the employee name.

## ALGORITHM :
1. Start the program.
2. Read the employee name from the user.
3. Create an Employee object and assign the name using the setName() method.
4. Return the current object using the display() method.
5. Display the employee name and stop the program.




## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Bharath Raj P
RegisterNumber:  212223230031
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class Employee {
    String name;
    void setName(String name) {
        this.name = name;
    }
    Employee display() {
        return this;
    }
    void printName() {
        System.out.println("Employee Name: "+name);
    }
}
class prog {
    public static void main(String[] args){
    Scanner sc = new Scanner(System.in);
    String str = sc.nextLine();
    Employee ob = new Employee();
    ob.setName(str);
    ob.display().printName();
    }
}
```





## OUTPUT:

<img width="618" height="189" alt="image" src="https://github.com/user-attachments/assets/dd154eff-cc7b-47a0-b2b8-10f82fb145e7" />


## RESULT:
Hence, the Java program for demonstrating the use of the this keyword was executed successfully and the employee name was displayed.
