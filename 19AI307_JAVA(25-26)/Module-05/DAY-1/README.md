# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in).

<img width="292" height="168" alt="image" src="https://github.com/user-attachments/assets/3f8d0eb2-c4df-4f52-9667-449f6d408f67" />

## AIM:
To write a Java program that reads user input using chained streams: BufferedReader → InputStreamReader → System.in.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a BufferedReader object by chaining it with an InputStreamReader.
4.	Read the name and age from the user.
5.	Convert age from string to integer.
6.	Display the user details.
7.	End the program.
   

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Tamizharasi S
RegisterNumber: 212222040170 
*/
```

## SOURCE CODE:
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class ChainingStreamsDemo {
    public static void main(String[] args) {
        try {
            BufferedReader br = new BufferedReader(
                    new InputStreamReader(System.in));

            String name = br.readLine();
            String age = br.readLine();

            System.out.println("--- User Details ---");
            System.out.println("Name: " + name);
            System.out.println("Age: " + age);

        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}

```
## OUTPUT:

<img width="735" height="322" alt="image" src="https://github.com/user-attachments/assets/c99f8a88-6d14-47c5-9084-e7c9988ea1cf" />

## RESULT:
Thus, the program to demonstrate chaining of streams using BufferedReader → InputStreamReader → System.in was successfully executed.
