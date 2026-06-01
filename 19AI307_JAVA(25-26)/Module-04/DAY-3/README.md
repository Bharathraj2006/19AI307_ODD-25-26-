# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

<img width="459" height="287" alt="image" src="https://github.com/user-attachments/assets/78bc0b13-d3c4-463f-ad0e-8f233da0d974" />

## AIM:

To write a Java program to demonstrate composition by managing books within a library.
## ALGORITHM :
1. Start the program.
2. Create a Library object and read the number of books from the user.
3. Read the title and author of each book.
4. Add each Book object to the Library using composition.
5. Display all books in the library and stop the program.
   
## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Bharath Raj P
RegisterNumber:  212223230031
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

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {
    private List<Book> books = new ArrayList<>();

    public void addBook(String title, String author) {
        Book book = new Book(title, author);
        books.add(book);
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books) {
            System.out.println("- " + b.getDetails());
        }
    }
}

```





## OUTPUT:
<img width="863" height="472" alt="image" src="https://github.com/user-attachments/assets/ced30760-afdd-4486-9c1a-29bbee130582" />



## RESULT:
Hence, the Java program for demonstrating composition using a Library and Book classes was executed successfully and the book details were displayed.
