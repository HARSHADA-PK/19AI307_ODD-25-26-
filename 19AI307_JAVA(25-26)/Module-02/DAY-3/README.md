# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

## AIM:
To write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create the BankAccount class with private variables and public getter/setter methods.
4.	In main(), create a BankAccount object.
5.	Read the account number and balance from the user.
6.	Set these values using setter methods.
7.	Display the account details using the display() method.
8.	End the program.


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
class BankAccount {
     private String accountNumber;
     private double balance;
     
     public String getAccountNumber() {
         return accountNumber;
     }
      public void setAccountNumber(String accountNumber) {
          this.accountNumber = accountNumber;
      }
       public double getBalance() {
           return balance;
          }
     public void setBalance(double balance) {
         this.balance = balance;
         }
    
}
public class main
{
    public static void main(String[] args)
    {
        Scanner input=new Scanner(System.in);
        BankAccount ob=new BankAccount();
        String num=input.nextLine();
        double bal=input.nextDouble();
        ob.setAccountNumber(num);
        ob.setBalance(bal);
        System.out.println("Account Number: "+ob.getAccountNumber());
        System.out.println("Balance: "+ob.getBalance());
    }
}

```


## OUTPUT:
<img width="822" height="373" alt="image" src="https://github.com/user-attachments/assets/53583a0e-fba0-4147-859c-0c12e07388b4" />


## RESULT:
Thus, the Java program demonstrating the use of access specifiers with private variables and public getter and setter methods was successfully executed.


