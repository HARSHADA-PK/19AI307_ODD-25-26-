# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is training to become a logic wizard. She enters a gate that tests her understanding of logical conditions.

She is given two magical conditions:

hasKey – whether she has the golden key (boolean)

knowsPassword – whether she knows the secret password (boolean)

The gate then evaluates her truthfulness using logical operators:

<img width="390" height="134" alt="image" src="https://github.com/user-attachments/assets/0660b40a-98a0-47bd-9151-2abc1a08e17d" />

Write a program that:

Accepts two boolean inputs: hasKey and knowsPassword

Displays the results of:

hasKey && knowsPassword
hasKey || knowsPassword
!hasKey
!knowsPassword
**Input Format:**

First line: true or false (hasKey)

Second line: true or false (knowsPassword)

**Output Format:**

Access with AND: <true/false>

Access with OR: <true/false>

Does NOT have key: <true/false>

Does NOT know password: <true/false>


## AIM:

To write a Java program that reads two integer numbers from the user and performs basic arithmetic operations such as addition, subtraction, multiplication, division, and modulus, and displays the results.

## ALGORITHM :
1. Start
2. Create a Scanner object to read input from the user.
3. Read two boolean values i and j from the user.
4. Compute the following:
       l1 = i && j → Logical AND of i and j
   
       l2 = i || j → Logical OR of i and j
   
       l3 = !i → Logical NOT of i
   
       l4 = !j → Logical NOT of j
   
5.Display the results:

      "Access with AND: " + l1

      "Access with OR: " + l2

       "Does NOT have key: " + l3

      "Does NOT know password: " + l4

6. Stop


## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Harshada P K
RegisterNumber:  212224060097
*/
```

## Sourcecode.java:
```
import java.util.*;
public class main
{
    public static void main(String[] args)
    {
        Scanner input=new Scanner(System.in);
        boolean hasKey=input.nextBoolean();
        boolean knowsPassword=input.nextBoolean();
        if(hasKey && knowsPassword)
        {
            System.out.println("Access with AND: true");
        }
        else{
            System.out.println("Access with AND: false");
        }
        if(hasKey || knowsPassword)
        {
             System.out.println("Access with OR: true");
        }
        else
        {
            System.out.println("Access with OR: false");
        }
        if(!hasKey)
        {
            System.out.println("Does NOT have key: true");
        }
        else
        {
            System.out.println("Does NOT have key: false");
        }
        if(!knowsPassword)
        {
            System.out.println("Does NOT know password: true");
        }
        else
        {
            System.out.println("Does NOT know password: false");
        }
    }
}
```





## OUTPUT:
<img width="848" height="415" alt="image" src="https://github.com/user-attachments/assets/47e4fe9b-ed37-4b1f-a010-fd6bb9f111fb" />


## RESULT:

The program has been executed successfully and the desired output has been obtained.
