# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

## AIM:
To write a Java program that defines a method cube(int x) which internally calls the method square(int x) to compute the cube of a number.

## ALGORITHM :
1. Define a class demo with two methods:

     square(int n) → returns n * n.
     cube(int n) → returns n * square(n) by calling the square() method internally.

2. In the main class, read an integer input from the user.

3. Create an object of the demo class.

4. Call the cube() method using the object and print the result.

5. End the program.





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
public class main
{
    public static int square(int x)
    {
        return x*x;
    }
    public static int cube(int x)
    {
        return x*square(x);
    }
    public static void main(String[] args)
    {
        Scanner input=new Scanner(System.in);
        int x=input.nextInt();
        int res=cube(x);
        System.out.println(res);
    }
}
```


## OUTPUT:
<img width="392" height="243" alt="image" src="https://github.com/user-attachments/assets/aa929a40-c871-4a15-8d09-12604778a14b" />



## RESULT:
The program has been executed successfully and the desired output has been obtained.

