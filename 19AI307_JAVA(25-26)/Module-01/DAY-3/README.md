# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

<img width="596" height="245" alt="image" src="https://github.com/user-attachments/assets/ec2959a3-9994-4f07-af8e-04433db7827e" />

## AIM:
To write a Java program that reads an integer and checks whether it is a palindrome number.

## ALGORITHM :
1.	Start the program.
2.	Create a Scanner object to read input.
3.	Read an integer num from the user.
4.	Store the number in a temporary variable originalNum.
5.	Reverse the number using a loop:
   Extract the last digit using % 10.
  	Build the reversed number.
  	Remove the last digit using / 10.
6. Compare the reversed number with the original number.
7. If both are equal, print that the number is a palindrome; otherwise, print it is not a palindrome.
8. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Tamizharasi S
RegisterNumber: 212222040170  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class PalindromeCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Input number
        int num = sc.nextInt();
        int originalNum = num;
        int reversed = 0;

        // Reverse the number
        while (num != 0) {
            int digit = num % 10;
            reversed = reversed * 10 + digit;
            num /= 10;
        }

        // Check palindrome
        if (originalNum == reversed) {
            System.out.println(originalNum + " is a Palindrome.");
        } else {
            System.out.println(originalNum + " is not a Palindrome.");
        }
    }
}

```
## OUTPUT:

<img width="1047" height="376" alt="image" src="https://github.com/user-attachments/assets/28d83adf-d483-4f33-aaad-f2eb2239c9f7" />

## RESULT:
Thus, the program successfully checks whether a given number is a palindrome and displays the correct output.
