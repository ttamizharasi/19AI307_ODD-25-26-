# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create a program that sends different types of notifications: "email", "sms", and "push". Use the Factory Pattern to generate the appropriate notification sender and call its notifyUser() method.

For example:

<img width="386" height="142" alt="image" src="https://github.com/user-attachments/assets/34eb7c90-6abb-4d98-9137-cb9e9ef1ca7a" />

## AIM:
To implement the Factory Design Pattern in Java to dynamically create and use different notification types such as Email, SMS, and Push notifications based on user input.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an interface Notification with the method notifyUser().
4.	Implement the interface in classes:(EmailNotification,SMSNotification,PushNotification)
5.	Create a NotificationFactory class with a method to generate appropriate notification objects.
6.	In the main class, read user input repeatedly until "exit" is entered.
7.	For each input, call the factory to create the correct notification object.
8.	Call the notifyUser() method of the created object.
9.	Display output.
10.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Tamizharasi S
RegisterNumber: 212222040170  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Notification {
    void notifyUser();
}

class EmailNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Email Notification");
    }
}

class SMSNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending SMS Notification");
    }
}

class PushNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Push Notification");
    }
}

class NotificationFactory {
    public Notification createNotification(String type) {
        switch (type.toLowerCase()) {
            case "email": return new EmailNotification();
            case "sms": return new SMSNotification();
            case "push": return new PushNotification();
            default: return null;
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        NotificationFactory factory = new NotificationFactory();

        while (true) {
            String input = sc.nextLine();
            if (input.equalsIgnoreCase("exit")) break;

            Notification n = factory.createNotification(input);
            if (n != null)
                n.notifyUser();
            else
                System.out.println("Invalid notification type: " + input);
        }
    }
}
```

## OUTPUT:

<img width="792" height="341" alt="image" src="https://github.com/user-attachments/assets/2b8a0108-011c-4dd8-b6be-a42eb020e9de" />

## RESULT:
Thus, the program successfully implements the Factory Design Pattern, creates notification objects dynamically based on user input, and displays the appropriate notification message.
