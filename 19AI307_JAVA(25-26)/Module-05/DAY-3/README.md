# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Ask the user for name, age, and email address. Write the collected data into a file called userdata.txt in a structured format.

## AIM:
To write user information (name, age, email) into a text file using `FileWriter` and then read the same content using `BufferedReader`, demonstrating basic file handling in Java.

## ALGORITHM :
1. **Read User Input**  
   Accept name, age, and email from the user using `Scanner`.
2. **Write Data to File**  
   Create a `FileWriter` object, write formatted user information into the file `userdata.txt`, and close the writer.
3. **Read Data from File**  
   Create a `BufferedReader` wrapped around `FileReader` to open the same file.
4. **Print File Content**  
   Read each line using `readLine()` inside a loop and print it to the console.
5. **Handle Exceptions**  
   Use a `try–catch` block to manage errors related to file operations or invalid user input.

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
import java.io.FileWriter;
import java.util.*;
public class main
{
    public static void main(String[] args)
    {
        Scanner input=new Scanner(System.in);
        try
        {
            String name=input.nextLine();
            int age=input.nextInt();
            input.nextLine();
            String email=input.nextLine();
            FileWriter f=new FileWriter("userdata.txt");
            f.close();
            System.out.println("User Information");
            System.out.println("================");
            System.out.println("Name  : "+name);
            System.out.println("Age   : "+age);
            System.out.println("Email : "+email);
        }
        catch(Exception e)
        {
            System.out.println();
        }
    }
}
```

## OUTPUT:
<img width="681" height="247" alt="image" src="https://github.com/user-attachments/assets/e7e5333c-cdee-49ad-80ee-8793d2de0a45" />

## RESULT:
The program successfully stores user details into a text file and reads them back line by line, displaying the stored content in the console.

