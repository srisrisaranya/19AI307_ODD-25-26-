# Ex.No:3(b) POLYMORPHISM

## QUESTION:

Write a Java program to create a class MaxFinder with three overloaded max() methods:

max(int a, int b) – returns the maximum of two integers.

max(double a, double b) – returns the maximum of two double values.

max(int a, int b, int c) – returns the maximum of three integers.

In the main() method, demonstrate the use of each overloaded method with various inputs.

## AIM:

To demonstrate method overloading in Java by finding the maximum value among two integers, two doubles, and three integers.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class MaxFinder with overloaded max() methods:
4. One method to find the maximum of two integers.
5. One method to find the maximum of two doubles.
6. One method to find the maximum of three integers.
7. Read two integer values from the user.
8. Read two double values from the user.
9. Read three integer values from the user.
10. Call the appropriate max() method for each set of inputs.
11. Display the maximum values.
12. Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class MaxFinder {
    int max(int a, int b) {
        return (a > b) ? a : b;
    }

    double max(double a, double b) {
        return (a > b) ? a : b;
    }

    int max(int a, int b, int c) {
        return (a > b && a > c) ? a : (b > c ? b : c);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        MaxFinder mf = new MaxFinder();

        // Read two integers
        int a1 = sc.nextInt();
        int b1 = sc.nextInt();

        // Read two doubles
        double d1 = sc.nextDouble();
        double d2 = sc.nextDouble();

        // Read three integers
        int a2 = sc.nextInt();
        int b2 = sc.nextInt();
        int c2 = sc.nextInt();

        System.out.println("Max(" + a1 + ", " + b1 + "): " + mf.max(a1, b1));
        System.out.println("Max(" + d1 + ", " + d2 + "): " + mf.max(d1, d2));
        System.out.println("Max(" + a2 + ", " + b2 + ", " + c2 + "): " + mf.max(a2, b2, c2));

        sc.close();
    }
}

```
## OUTPUT:

<img width="891" height="496" alt="image" src="https://github.com/user-attachments/assets/e411fd3a-c5c7-422c-b349-07a3030a3f5b" />


## RESULT:
The program successfully demonstrates method overloading by using different versions of the max() method to find and display the maximum values for different types and numbers of inputs.
