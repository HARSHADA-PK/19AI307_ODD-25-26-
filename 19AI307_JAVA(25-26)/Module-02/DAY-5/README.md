# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Define class Game with: Static variable maxScore = 500 Print max score via 3 different object references. Change via one object into 800, and print the output of previous maxScore and changed maxScore. 

## AIM:
To define class Game with: Static variable maxScore = 500 Print max score via 3 different object references. Change via one object into 800, and print the output of previous maxScore and changed maxScore. 

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	In the main() method, create three objects of Game.
4.	Print maxScore using all three objects.
5.	Modify maxScore to 800 using one object.
6.	Print the updated value using all three objects.
7.	End the program.

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
class game
{
    static int max=500;
}
public class main
{
    public static void main(String[] args)
    {
        game g1=new game();
        game g2=new game();
        game g3=new game();
        System.out.println(g1.max);
        System.out.println(g2.max);
        System.out.println(g3.max);
        
        g1.max=800;
        System.out.println(g1.max);
        System.out.println(g2.max);
        System.out.println(g3.max);
    }
}
```


## OUTPUT:
<img width="287" height="283" alt="image" src="https://github.com/user-attachments/assets/1c35e3a4-9e6b-4bdc-8371-bcb87e4f52ba" />


## RESULT:
Thus, the Java program demonstrating the use of the static access modifier with multiple object references was successfully executed.


