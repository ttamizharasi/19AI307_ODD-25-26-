# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to demonstrate the use of a default constructor and display a message from it.

<img width="662" height="173" alt="image" src="https://github.com/user-attachments/assets/4acb6b2b-8dfe-41a8-bcf6-68b4351c9500" />

## AIM:
To write a Java program that demonstrates the use of a default constructor and displays a welcome message using variable scope.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare a class with a string variable for storing the name.
4.	Create a default constructor that prints a welcome message.
5.	Read a name input from the user.
6.	Create an object of the class by passing the name.
7.	Display the message from the default constructor.
8.	End the program.


## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Tamizharasi S
RegisterNumber: 212222040170 
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class Welcome 
{
    String name;
    Welcome(String name) {
        this.name = name;
        System.out.println("Welcome, " + name + "! This is the default constructor.");
    }
}

public class Main1 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        Welcome obj = new Welcome(name);
    }
}

```

## OUTPUT:

<img width="1163" height="348" alt="image" src="https://github.com/user-attachments/assets/76538a2e-48b5-40c6-8ba8-06d585e1c7b1" />

## RESULT:
Thus, the program successfully demonstrates the use of a default constructor and displays a welcome message.
