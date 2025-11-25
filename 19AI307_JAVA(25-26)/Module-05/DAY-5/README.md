# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Use a thread pool to calculate and print the square of each number from input.

Input :

3 2 4 5
Output:

Square: 4
Square: 16
Square: 25

For example:

<img width="290" height="167" alt="image" src="https://github.com/user-attachments/assets/4c1835e6-50d8-44bf-a723-c49800c5f2f2" />

## AIM:
To write a Java program that uses a thread pool to calculate the square of each number entered by the user.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a fixed thread pool using Executors.newFixedThreadPool().
4.	Continuously read integers from the user.
5.	For each number, submit a task to the thread pool that computes its square.
6.	Print the result from each task.
7.	Shutdown the thread pool.
8.	End the program.
   

## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Tamizharasi S
RegisterNumber: 212222040170 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;
import java.util.concurrent.TimeUnit;

public class SquareCalculatorFixed {
    public static void main(String[] args) throws InterruptedException {
        Scanner sc = new Scanner(System.in);

     
        int n = sc.nextInt();
        ExecutorService executor = Executors.newSingleThreadExecutor();

        for (int i = 0; i < n; i++) {
            int num = sc.nextInt(); 

            executor.submit(() -> {
                System.out.println("Square: " + (num * num));
            });
        }

        executor.shutdown();
        executor.awaitTermination(5, TimeUnit.SECONDS);
    }
}

```
## OUTPUT:

<img width="487" height="492" alt="image" src="https://github.com/user-attachments/assets/7af92ef8-14ec-4810-b978-c2ad192587b3" />

## RESULT:
Thus, the program successfully computes the square of each number using a thread pool and displays the result.
