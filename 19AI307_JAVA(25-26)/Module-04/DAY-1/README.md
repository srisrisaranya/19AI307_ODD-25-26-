# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.

## AIM:

To perform integer division in Java and handle division-by-zero exceptions using exception handling.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the dividend and divisor from the user.
4. Perform the division operation (dividend / divisor).
5. If the divisor is zero:
Catch the ArithmeticException.
Display "Error: Division by zero".
6. Otherwise, display the result.
7. Close the scanner.
8. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.util.Scanner; 
public class IntegerDivision {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        try {
            int dividend = scanner.nextInt(); 
            int divisor = scanner.nextInt(); 
            int result = dividend / divisor;
            System.out.println("Result: " + result);

        } catch (ArithmeticException e) {
            System.out.println("Error: Division by zero");
        } catch (java.util.InputMismatchException e) {
        } finally {
            scanner.close();
        }
    }
}

```
## OUTPUT:

<img width="861" height="417" alt="image" src="https://github.com/user-attachments/assets/3ebcc8eb-a52e-4184-b915-526168c69d7b" />

## RESULT:
The program successfully performs integer division and handles division-by-zero errors using exception handling, preventing the program from crashing.
