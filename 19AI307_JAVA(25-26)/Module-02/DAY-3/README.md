# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Rectangle with private instance variables length and width. Provide public getter and setter methods to access and modify these variables

## AIM:
To write a Java program to demonstrate encapsulation using a Rectangle class with private data members and getter/setter methods.

## ALGORITHM :
1. Start the program.
2. Create a Rectangle class with private variables length and width.
3. Use setter methods to assign values to length and width.
4. Use getter methods to retrieve the values of length and width.
5. Display the length and width and stop the program.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Rectangle {
  private double length;
  private double width;
  public double getLength() {return length; } 
  public void setLength(double length) {this.length = length; }
  public double getWidth() {return width; } 
  public void setWidth(double width) {this.width = width; }
  public double calculateArea() {return length * width; }}
public class main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        double length = sc.nextDouble();
        double width = sc.nextDouble();
        Rectangle o = new Rectangle();
        o.setLength(length);
        o.setWidth(width);
        System.out.println("Length: "+o.getLength());
        System.out.println("Width: "+o.getWidth());
 }
}

```

## OUTPUT:
<img width="547" height="246" alt="image" src="https://github.com/user-attachments/assets/09cf4d17-0294-43ca-86a9-7b241c4bca05" />



## RESULT:
Hence, the Java program for demonstrating encapsulation using getter and setter methods was executed successfully and the values were displayed.
