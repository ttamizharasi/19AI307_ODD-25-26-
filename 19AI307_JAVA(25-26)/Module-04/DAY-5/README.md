# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Build a simple Air Traffic Control System where multiple Airplane objects request landing through a central mediator.
For example:

<img width="568" height="381" alt="image" src="https://github.com/user-attachments/assets/55428e69-866e-4a3f-870d-65b09edad874" />

## AIM:
To implement a Behavioural Design Pattern (Mediator Pattern) using Java, where multiple Airplane objects communicate through a central AirTrafficControl mediator to manage landing requests.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a mediator class AirTrafficControl to manage runway availability.
4.	Add a method requestLanding() to grant/deny landing permission.
5.	Create an Airplane class that interacts with the mediator.
6.	Read the number of airplanes and runway release mode (true/false).
7.	Read airplane names and create Airplane objects.
8.	Each airplane requests landing through the mediator.
9.	Display the landing granted or denied message.
10.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Tamizharasi S
RegisterNumber: 212222040170
*/
```

## SOURCE CODE:

```
import java.util.*;

class AirTrafficControl {
    private boolean runwayFree = true;

    public boolean requestLanding(Airplane airplane) {
        if (runwayFree) {
            runwayFree = false;
            System.out.println(airplane.getName() + " granted landing.");
            return true;
        } else {
            System.out.println(airplane.getName() + " denied landing. Runway busy.");
            return false;
        }
    }

    public void releaseRunway() {
        runwayFree = true;
    }
}

class Airplane {
    private String name;
    private AirTrafficControl control;

    public Airplane(String name, AirTrafficControl control) {
        this.name = name;
        this.control = control;
    }

    public String getName() {
        return name;
    }

    public void requestLanding(boolean releaseAfterLanding) {
        boolean allowed = control.requestLanding(this);
        if (allowed) {
            System.out.println(name + " landed successfully.");
            if (releaseAfterLanding) {
                control.releaseRunway();
            }
        }
    }
}

public class AirTrafficSystem {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        AirTrafficControl control = new AirTrafficControl();

        int n = Integer.parseInt(sc.nextLine()); // number of airplanes
        boolean release = sc.nextLine().equalsIgnoreCase("true"); // release after landing?

        List<Airplane> airplanes = new ArrayList<>();
        for (int i = 0; i < n; i++) {
            String name = sc.nextLine();
            airplanes.add(new Airplane(name, control));
        }

        for (Airplane plane : airplanes) {
            plane.requestLanding(release);
        }

        sc.close();
    }
}

```

## OUTPUT:

<img width="1181" height="622" alt="image" src="https://github.com/user-attachments/assets/43372791-9461-4607-8e68-73d915693408" />

## RESULT:
Thus, the program successfully implements the Mediator Behavioural Design Pattern, where a central AirTrafficControl system coordinates landing requests from multiple airplanes.
