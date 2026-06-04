# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:

Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

## AIM:

To demonstrate composition in Java by creating a Library class that contains multiple Book objects.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Library object.
4. Read the number of books n.
5. Repeat n times:
6. Read the book title.
7. Read the author name.
8. Create a Book object.
9. Add the Book object to the library.
10. Call the showBooks() method.
11. Display all books stored in the library.
12. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Saranya S 
RegisterNumber:  212223110044
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
    private List<Book> books;
    public Library() {
        books = new ArrayList<>();
    }
    public void addBook(String title, String author) {
        // Type Your Code Here
        Book book = new Book(title, author); 
        books.add(book);
    }
    public void showBooks() {
        // Type Your Code Here
        System.out.println("Books in Library:");
        if (books.isEmpty()) {
            System.out.println("No books available.");
        } else {
            for (Book b : books) {
                System.out.println("- " + b.getDetails());
            }
        }
    }
}



```
## OUTPUT:

<img width="1150" height="637" alt="image" src="https://github.com/user-attachments/assets/7ba4afb7-8806-4aa8-bea8-999dbbe63a46" />


## RESULT:
The program successfully demonstrates composition by storing multiple Book objects inside a Library object and displaying the details of all books in the library.
