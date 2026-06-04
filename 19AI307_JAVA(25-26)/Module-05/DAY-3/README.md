# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:

Write a Java program to write a string to a text file named output.txt.

## AIM:

To write text into a file using the FileWriter class in Java.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a FileWriter object for the file output.txt.
4. Write the given text into the file.
5. Close the file using the close() method.
6. Display a success message.
7. If an error occurs, catch the IOException and display an error message.
8. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.io.IOException;
import java.util.*;
public class WriteToFile {
    public static void main(String[] args) {
        try {
            FileWriter writer = new FileWriter("output.txt");
            writer.write("Hello, this is a sample text written to the file.");
            writer.close();

            System.out.println("Successfully wrote to the file.");
        } catch (IOException e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }
    }
}
```
## OUTPUT:

<img width="932" height="252" alt="image" src="https://github.com/user-attachments/assets/1bbc6b2d-3c23-437c-aa27-0ec6423e3c46" />


## RESULT:
The program successfully writes the text "Hello, this is a sample text written to the file." into output.txt and displays a success message.
