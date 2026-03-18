# Ex.No:5(E) MULTITHREADING - SYNCHRONIZATION

## QUESTION:
Synchronize deposit method in a BankAccount class, simulate deposits from multiple threads.

**Input:**

3 100 200 300

**Output:**

Final Balance: 600

## AIM:
To simulate multiple concurrent deposits into a shared bank account using threads, ensuring thread-safety by synchronizing the deposit method.

## ALGORITHM :
1. Create a `BankAccount` class with a `balance` variable and a synchronized `deposit(int amount)` method.  
2. Create a `DepositTask` class extending `Thread`, storing a reference to `BankAccount` and the deposit amount, and call `deposit()` inside `run()`.  
3. In `main`, read `n` (number of deposits), then read each deposit amount and create/start a thread for each.  
4. Use `join()` on all threads to ensure all deposits are completed.  
5. Print the final bank balance using `getBalance()`.

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

class BankAccount {
    int balance = 0;

    synchronized void deposit(int amount) {
        balance = balance + amount;
    }
}

class MyThread extends Thread {
    BankAccount acc;
    int amt;

    MyThread(BankAccount acc, int amt) {
        this.acc = acc;
        this.amt = amt;
    }

    public void run() {
        acc.deposit(amt);
    }
}

public class Main {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        BankAccount acc = new BankAccount();

        MyThread[] t = new MyThread[n];

        for (int i = 0; i < n; i++) {
            int amount = sc.nextInt();
            t[i] = new MyThread(acc, amount);
            t[i].start();
        }

        for (int i = 0; i < n; i++) {
            t[i].join();
        }

        System.out.println("Final Balance: " + acc.balance);
    }
}
```

## OUTPUT:
<img width="628" height="450" alt="image" src="https://github.com/user-attachments/assets/6ce76abd-fa5b-4743-b7e0-a9e0b46389da" />

## RESULT:
The program safely performs concurrent deposits using synchronized access and prints the correct final balance.

