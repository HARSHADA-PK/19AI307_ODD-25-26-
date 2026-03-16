# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Vehicle with attributes as number, type and owner.

## AIM:
To Create a class Vehicle with attributes as number, type and owner.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Import the package java.util.Scanner to read user input.
4.	Create a class Vehicle with data members: (number, type, owner).
5.	In the main() method, create a Scanner object.
6.	Create two objects of the Vehicle class.
7.	Read the details (number, type, owner) for both objects from user input.
8.	Display the details of both vehicles.

## PROGRAM:
```
/*
Program to implement a conditional statement using Java
Developed by: Harshada P K
RegisterNumber:  212224060097
*/
```

## SOURCE CODE:
```python
import java.util.Scanner;
class Vehicle
{
    String number;
    String type;
    String owner;
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Vehicle v1 = new Vehicle();
        v1.number = sc.next();
        v1.type = sc.next();
        v1.owner = sc.next();

        Vehicle v2 = new Vehicle();
        v2.number = sc.next();
        v2.type = sc.next();
        v2.owner = sc.next();

        System.out.println(v1.number + " | " + v1.type + " | " + v1.owner);
        System.out.println(v2.number + " | " + v2.type + " | " + v2.owner);
    }
}

```


## OUTPUT:
<img width="900" height="270" alt="image" src="https://github.com/user-attachments/assets/f8664cb3-2be8-4087-90ff-8070fabf217d" />


## RESULT:
Thus, a Java program to create a class Vehicle with attributes number, type, and owner was successfully implemented and executed.

