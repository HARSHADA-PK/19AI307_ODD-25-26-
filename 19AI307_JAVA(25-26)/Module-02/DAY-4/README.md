# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a class that uses a constructor to initialize variables and overrides toString() method.

## AIM:
To write a Java program that initializes object variables using a constructor and overrides the toString() method to display object details in a readable format.

## ALGORITHM :

1. Define a class Student with two instance variables:

     String name

     int age

2. Create a parameterized constructor to initialize these variables.

3. Override the toString() method to return the student details in a formatted string.

4. In the main() method:

    - Read the name and age from the user.

    - Create a Student object using the constructor.

5. Print the object, which automatically calls the overridden toString() method.

6. End the program.



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
class student
{
    String name;
    int age;
    student(String name,int age)
    {
        this.name=name;
        this.age=age;
    }
    public String toString()
    {
        return "Student{name='"+name+"', age="+age+"}";
    }
}
public class main
{
    public static void main(String[] args)
    {
        Scanner input=new Scanner(System.in);
        String name=input.nextLine();
        int age=input.nextInt();
        student ob=new student(name,age);
        System.out.println(ob);
    }
}
```




## OUTPUT:
<img width="896" height="395" alt="image" src="https://github.com/user-attachments/assets/0b280b01-a09a-4749-b733-41411f01b00a" />




## RESULT:
The program has been executed successfully and the desired output has been obtained.

