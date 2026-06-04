# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:

Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)

## AIM:

To demonstrate chaining of input streams in Java using BufferedReader and InputStreamReader to read and display user details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an InputStreamReader object connected to System.in.
4. Chain it with a BufferedReader object.
5. Read the user's name.
6. Read the user's age.
7. Convert the age from string to integer.
8. Display the user's name and age.
9. Handle any input/output exceptions.
10. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class ChainingStreamsExample {
    public static void main(String[] args) {
        
        // Chaining streams
        BufferedReader br = new BufferedReader(
                                new InputStreamReader(System.in));

        try {
            // Read name
            String name = br.readLine();

            // Read age
            int age = Integer.parseInt(br.readLine());

            // Display output
            System.out.println("--- User Details ---");
            System.out.println("Name: " + name);
            System.out.println("Age: " + age);

        } catch (IOException e) {
            System.out.println("Error occurred.");
        }
    }
}
```

## OUTPUT:

<img width="952" height="580" alt="image" src="https://github.com/user-attachments/assets/23966c76-eb73-4dd6-8e24-3669f8786d47" />


## RESULT:
The program successfully demonstrates stream chaining by using BufferedReader and InputStreamReader to read user input and display the user's details.
