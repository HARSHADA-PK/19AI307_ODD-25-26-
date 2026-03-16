# Ex.No:3(B) POLYMORPHISM

## QUESTION:
Write a Java program using method overloading to print student details. Create a class Student with:

- print(String name)

- print(String name, int age)

- print(String name, int age, String dept)

## AIM:
To write a Java program that demonstrates method overloading by printing student details using three versions of the `print()` method with different parameter lists.

## ALGORITHM :
1. Create a class `Student` with three overloaded static methods:
   - `print(String name)`
   - `print(String name, int age)`
   - `print(String name, int age, String dept)`
2. In the `main` method:
   - Create a `Scanner` object to read input.
   - Read a name and call `print(name)`.
   - Read a name and age, then call `print(name, age)`.
   - Read a name, age, and department, then call `print(name, age, dept)`.
3. Each method prints the student details according to the parameters provided.
4. End the program.

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
import java.util.Scanner;

public class Student {
    public static void print(String name) {
        System.out.println("Name: " + name);
    }

    public static void print(String name, int age) {
        System.out.println("Name: " + name + ", Age: " + age);
    }

    public static void print(String name, int age, String dept) {
        System.out.println("Name: " + name + ", Age: " + age + ", Dept: " + dept);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String name1 = scanner.nextLine();
        print(name1);

        String name2 = scanner.nextLine();
        int age2 = scanner.nextInt();
        scanner.nextLine(); 
        print(name2, age2);

        String name3 = scanner.nextLine();
        int age3 = scanner.nextInt();
        scanner.nextLine();
        String dept3 = scanner.nextLine();
        print(name3, age3, dept3);
    }
}
```

## OUTPUT:
<img width="850" height="603" alt="image" src="https://github.com/user-attachments/assets/a78d9cb1-9f34-4ec6-a285-fc784d35ee62" />

## RESULT:
The program successfully demonstrates method overloading by printing student details using three different method signatures based on the number of arguments passed.


