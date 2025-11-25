# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely found a magic machine that tells her how two numbers relate to each other.
The machine supports all 6 relational operators:

Operator	Meaning
==	Is equal to
!=	Is not equal to
>	Greater than
<	Less than
>=	Greater than or equal to
<=	Less than or equal to
Lovely enters two numbers. The machine prints the result (true or false) for each operator.

Input Format
First line: First integer number (a)

Second line: Second integer number (b)

Output Format
Print:

a == b: <true/false>
a != b: <true/false>
a > b: <true/false>
a < b: <true/false>
a >= b: <true/false>
a <= b: <true/false>

For example:


<img width="316" height="223" alt="image" src="https://github.com/user-attachments/assets/7a680d81-ca68-42b6-97c2-2a750e6f47ba" />

## AIM:
To write a Java program that reads two integers and evaluates all relational operators between them.

## ALGORITHM :
1.	Start the program.
2.	Create a Scanner object to read input.
3.	Read two integer values a and b from the user.
4.	Evaluate the following relational expressions:
     a == b
  	  a != b
     a > b
     a < b
     a >= b
     a <= b
5. Print the results in the required format.
6. Stop the program.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Tamizharasi S
RegisterNumber:  212222040170
*/
```

## Sourcecode.java:

```
import java.util.Scanner;

public class RelationalCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Input integers
        int a = sc.nextInt();
        int b = sc.nextInt();

        // Relational operations
        System.out.println("a == b: " + (a == b));
        System.out.println("a != b: " + (a != b));
        System.out.println("a > b: " + (a > b));
        System.out.println("a < b: " + (a < b));
        System.out.println("a >= b: " + (a >= b));
        System.out.println("a <= b: " + (a <= b));
    }
}

```
## OUTPUT:

<img width="1230" height="365" alt="image" src="https://github.com/user-attachments/assets/f6239e06-3f05-42a3-bd32-c4beac3783eb" />

## RESULT:
Thus, the program successfully evaluates all relational operators for two integers and prints the correct results.


