# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

## AIM:
To write a Java program that demonstrates **composition**, where a `Library` contains multiple `Book` objects.  
The program should accept book details from the user, store them inside a `Library` object, and display all stored books.

## ALGORITHM :
1. Start the program.
2. Create a `Book` class with:
   - Private attributes: `title`, `author`
   - Constructor to initialize them
   - Method `getDetails()` returning formatted book details
3. Create a `Library` class that contains:
   - A `List<Book>` to store books
   - `addBook(title, author)` method to add a new book to the list
   - `showBooks()` method to print all books
4. In the `main` method:
   - Create a `Scanner` object
   - Create a `Library` object
   - Read integer `n` → number of books
   - Loop `n` times:
     - Read book title
     - Read author name
     - Add the book to the library
   - Call `library.showBooks()` to display all stored books
   - Close the scanner
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

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();
        int n = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }
        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    String getDetails() {
        return "- " + title + " by " + author;
    }
}

class Library {
    private List<Book> books;

    Library() {
        books = new ArrayList<>();
    }

    void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books)
            System.out.println(b.getDetails());
    }
}
```

## OUTPUT:
<img width="1065" height="589" alt="image" src="https://github.com/user-attachments/assets/d87a464b-6f1a-4759-a6f7-e74206df169a" />

## RESULT:
The program successfully demonstrates **composition** by creating a `Library` object that holds multiple `Book` objects. It reads book details from the user, stores them inside the library, and displays all the books in a structured format.


