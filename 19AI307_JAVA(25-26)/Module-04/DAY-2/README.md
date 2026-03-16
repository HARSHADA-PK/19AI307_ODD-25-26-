# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.

To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.

Your task is to simulate this system using the Singleton pattern.

**Key Hint (Hidden in Story):**
Only one control tower object should exist.

Every flight contacting it should register its name.

You should log the order of flights that contacted the tower.

## Input Format:
First line: Integer n – number of incoming flights

Next n lines: Each line contains the flight name.

## Output Format:
For each flight, print:

`[FlightName] registered with Radar Control Tower. Total Flights: [count]`

## AIM:
To simulate an airport Radar Control Tower system using the **Singleton design pattern**, ensuring that all incoming flights communicate with the same single instance of the control tower.

## ALGORITHM :
1. Create a `RadarControlTower` class.
2. Declare a private static instance variable to hold the single tower object.
3. Make the constructor **private** to prevent external instantiation.
4. Implement the `getInstance()` method:
   - If the instance is `null`, create a new `RadarControlTower`.
   - Otherwise, return the existing instance.
5. Maintain a `flightCount` variable to track how many flights have registered.
6. Implement `registerFlight(String flightName)`:
   - Increment `flightCount`
   - Return the updated count.
7. In the `main` method:
   - Read the number of incoming flights `n`.
   - For each flight:
     - Read the flight name.
     - Get the single instance of the Radar Control Tower.
     - Register the flight.
     - Print:  
       `[FlightName] registered with Radar Control Tower. Total Flights: [count]`
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Harshada P K
RegisterNumber:  212224060097
*/
```
## SOURCE CODE:
```
import java.util.*;

class RadarControlTower {
    private static RadarControlTower instance;
    private int flightCount = 0;

    private RadarControlTower() {}

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
        sc.nextLine();  // consume newline

        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance();
            int total = tower.registerFlight(flight);
            System.out.println(flight + " registered with Radar Control Tower. Total Flights: " + total);
        }
    }
}
```

## OUTPUT:

<img width="1161" height="200" alt="image" src="https://github.com/user-attachments/assets/da246116-cf22-4787-b17d-917de4660a7a" />

## RESULT:

The program successfully demonstrates the **Singleton pattern** by ensuring that all flights use the same Radar Control Tower instance. It registers each flight in order and displays the current total number of flights handled by the tower.


