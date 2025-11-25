# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.

To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.

Your task is to simulate this system using the Singleton pattern.

Key Hint (Hidden in Story):
Only one control tower object should exist.

Every flight contacting it should register its name.

You should log the order of flights that contacted the tower.

Input Format:
First line: Integer n – number of incoming flights
Next n lines: Each line contains the flight name.

Output Format:
For each flight, print:
[FlightName] registered with Radar Control Tower. Total Flights: [count]

For example:

<img width="637" height="172" alt="image" src="https://github.com/user-attachments/assets/09c23cbf-4ff7-4ac1-829e-2a164b446cfc" />


## AIM:
To implement a Singleton pattern in Java to simulate a Radar Control Tower where only one tower instance exists, and all flights register with it.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a RadarControlTower class with a private static instance.
4.	Make the constructor private to prevent multiple instances.
5.	Implement a getInstance() method to return the single instance.
6.	Add a method registerFlight(String flightName) to register a flight and increment flight count.
7.	Read the number of flights n.
8.	For each flight:

Read the flight name.

Get the singleton tower instance.

Register the flight and display total registered flights.


## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Tamizharasi S
RegisterNumber:  212222040170
*/
```

## SOURCE CODE:


```
import java.util.*;

class RadarControlTower {
    private static RadarControlTower instance = null;
    private int flightCount;

    private RadarControlTower() {
        flightCount = 0;
    }

    public static RadarControlTower getInstance() {
        if (instance == null) {
            instance = new RadarControlTower();
        }
        return instance;
    }

    public int registerFlight(String flightName) {
        flightCount++;
        return flightCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance();
            int total = tower.registerFlight(flight);
            System.out.println(flight + " registered with Radar Control Tower. Total Flights: " + total);
        }
        sc.close();
    }
}

```

## OUTPUT:

<img width="1269" height="418" alt="image" src="https://github.com/user-attachments/assets/8cbea607-d00e-4f3f-858a-649c1f50321e" />


## RESULT:

The program successfully demonstrates the Singleton pattern, ensuring only one Radar Control Tower instance exists and all flights register through it, maintaining consistent flight tracking.

