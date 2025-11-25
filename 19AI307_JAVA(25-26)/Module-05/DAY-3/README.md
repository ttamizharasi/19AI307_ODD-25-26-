# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Read a file and print only the lines containing the word "Java".
For example:

<img width="472" height="145" alt="image" src="https://github.com/user-attachments/assets/cb8a926f-4c1a-4a04-b1db-220c9744a3eb" />

## AIM:
To write a Java program that reads input lines from the user, stores them in a file, and then prints only the lines containing the word Java.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a file to store input text.
4.	Continuously read lines from the user until the user enters "exit".
5.	Write each line into the file.
6.	After writing, open the file using BufferedReader.
7.	Read each line and check if it contains the word "Java".
8.	If it does, print that line.
9.	Close all streams and end the program.
    

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Tamizharasi S
RegisterNumber: 212222040170 
*/
```

## SOURCE CODE:
```
import java.io.*;

public class JavaFilterLines {
    public static void main(String[] args) {
        try (BufferedReader br = new BufferedReader(new InputStreamReader(System.in))) {
        
            System.out.println("Lines containing the word 'Java':");

            String line;
            while (!(line = br.readLine()).equals("exit")) {
                if (line.contains("Java")) {
                    System.out.println(line);
                }
            }
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}

```
## OUTPUT:

<img width="1062" height="357" alt="image" src="https://github.com/user-attachments/assets/ab441ae0-99f7-46d1-8c5a-c92f150cb441" />

## RESULT:
Thus, the program to filter and print lines containing the word "Java" was successfully executed.
