# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program demonstrating method overriding. Create a class Animal with a method sound(). Subclass it as Dog, Cat, Cow, each overriding the sound() method.
For example:

<img width="290" height="97" alt="image" src="https://github.com/user-attachments/assets/d733cb22-859f-415c-9b28-111147bc8517" />

## AIM:
To write a Java program that demonstrates method overriding using a base class (Animal) and its subclasses (Dog, Cat, Cow), each providing its own implementation of the sound() method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a base class Animal with a method sound().
4.	Create derived classes Dog, Cat, and Cow that override the sound() method.
5.	Read an input string (animal name) from the user.
6.	Based on the input, create the corresponding subclass object.
7.	Call the overridden sound() method using dynamic method dispatch.
8.	Display the result.
9.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Tamizharasi S
RegisterNumber: 212222040170 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Animal {
    public void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    public void sound() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    public void sound() {
        System.out.println("Cat meows");
    }
}

class Cow extends Animal {
    public void sound() {
        System.out.println("Cow moos");
    }
}

public class AnimalSound {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Animal a;

        String input = scanner.nextLine().trim().toLowerCase();

        switch (input) {
            case "dog":
                a = new Dog();
                break;
            case "cat":
                a = new Cat();
                break;
            case "cow":
                a = new Cow();
                break;
            default:
                System.out.println("Unknown animal");
                scanner.close();
                return;
        }

        a.sound();
        scanner.close();
    }
}

```
## OUTPUT:

<img width="952" height="350" alt="image" src="https://github.com/user-attachments/assets/80b6d684-98a5-4315-9e84-bcaa12e39c0e" />

## RESULT:
Thus, the Java program successfully demonstrates method overriding using the Animal, Dog, Cat, and Cow classes, and prints the correct sound based on the object created.
