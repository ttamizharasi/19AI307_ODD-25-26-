# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.
Note : Read the threadname from the User
For example:

<img width="382" height="157" alt="image" src="https://github.com/user-attachments/assets/3cbb5bfb-9f7b-4063-bcae-fd54089125bd" />

## AIM:
To write a Java program that sets the thread name based on user input and displays the thread’s name, priority, and full thread information.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the thread name from the user.
4.	Get the current thread using Thread.currentThread().
5.	Set the name of the thread to the user-entered value.
6.	Get and display the thread priority.
7.	Display the thread name.
8.	Print the full thread details using toString().
9.	End the program.
    

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Tamizharasi S
RegisterNumber:  212222040170
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class CurrentThreadInfo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();
        Thread t = Thread.currentThread();
        t.setName(threadName);

        
        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);

        sc.close();
    }
}

```
## OUTPUT:

<img width="742" height="227" alt="image" src="https://github.com/user-attachments/assets/83915a6a-b5d1-491f-9903-2e140ec06629" />

## RESULT:
Thus, the program to determine and display the priority and name of the current thread was successfully executed.
