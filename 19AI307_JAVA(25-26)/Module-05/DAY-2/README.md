# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a program to demonstrate reading UTF strings using DataInputStream.

<img width="427" height="122" alt="image" src="https://github.com/user-attachments/assets/1829279e-fcf6-4733-9c2d-0c8c4092a2f8" />

## AIM:
To write a Java program that reads a UTF string from a file using DataInputStream after writing it using DataOutputStream.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package java.io.* and java.util.*.
3.	Read a string from the user.
4.	Create a DataOutputStream object and write the UTF string to a file.
5.	Close the output stream.
6.	Create a DataInputStream object to read the UTF string from the file.
7.	Display the retrieved UTF string.
8.	Close the input stream.
9.	End the program.
    

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Tamizharasi S
RegisterNumber: 212222040170  
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.Scanner;

public class DataInputStreamUTFExample {
    public static void main(String[] args) {
        String fileName = "utfdata.dat";
        Scanner scanner = new Scanner(System.in);

        try {
            String input = scanner.nextLine();

            DataOutputStream dos = new DataOutputStream(new FileOutputStream(fileName));
            dos.writeUTF(input);
            dos.close();

            DataInputStream dis = new DataInputStream(new FileInputStream(fileName));
            String result = dis.readUTF();
            dis.close();

            System.out.println("String read from file: " + result);
        } catch (Exception e) {
            System.out.println("Error: " + e.getMessage());
        } finally {
            scanner.close();
        }
    }
}

```
## OUTPUT:

<img width="800" height="277" alt="image" src="https://github.com/user-attachments/assets/ddddb475-294a-42f2-a215-f72ae026b188" />

## RESULT:
Thus, the program to read UTF strings using DataInputStream was successfully executed.
