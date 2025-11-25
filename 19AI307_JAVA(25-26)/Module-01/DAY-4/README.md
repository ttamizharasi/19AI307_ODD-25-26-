# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the index of a given element in an array

For example:

<img width="330" height="378" alt="image" src="https://github.com/user-attachments/assets/9d84d067-6c65-4565-b457-16bbe65a0dac" />

## AIM:
To write a Java program that reads an array of integers and finds the index of a given element.

## ALGORITHM :
1.	Start the program.
2.	Create a Scanner object to read user input.
3.	Read the size of the array n.
4.	Declare an integer array and read n elements from the user.
5.	Read the element to be searched.
6.	Traverse the array:
    If an element matches the search value, store its index and stop the search.
7. If the element is found, print its index.
8. Otherwise, print "Element not found".
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: Tamizharasi S
RegisterNumber: 212222040170
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        boolean found = false;
        int[] arr = new int[n];
        int index = 0;
        for(int i=0;i<n;i++)
        {
            arr[i] = sc.nextInt();
        }
        int num = sc.nextInt();
        for(int i=0;i<n;i++)
        {
            if(arr[i]==num)
            {
                found = true;
                index = i;
            }
        }
        if(found==false)
        {
            System.out.print("Element not found");
        }
        else{
            System.out.print(index);
        }
    }
}

```
## OUTPUT:

<img width="897" height="556" alt="image" src="https://github.com/user-attachments/assets/f90afd5d-1675-492e-b809-ef46e0596cb9" />

## RESULT:
Thus, the program successfully finds the index of a given element in an array and prints the correct result.
