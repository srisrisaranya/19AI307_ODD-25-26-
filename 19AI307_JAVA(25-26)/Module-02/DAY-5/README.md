# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:

Create a class `MathConstants` and declare `PI` as a final variable. Try changing it and see the result.

## AIM:

To demonstrate the use of a final variable in Java.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare a final variable PI and assign a value.
4. Create an object of the class.
5. Call the displayPI() method.
6. Display the value of PI.
7. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
class prog {
    final double PI = 3.14159;
void tryToChange() {
    // Try to change PI here (commented out because it causes error)
    // PI = 3.14;
    }
void displayPI() {
    // Print PI here
    System.out.println(PI);
    }
 public static void main(String[] args) {
     prog obj = new prog();
     // call displayPI here
     obj.displayPI();
     // optionally call tryToChange (but causes error)
     }
}
```
## OUTPUT:

<img width="677" height="267" alt="image" src="https://github.com/user-attachments/assets/fe14b195-0b4f-4f97-84ac-1eadea2f3dc1" />


## RESULT:
The program successfully displays the value of the final variable PI, showing that its value cannot be changed once assigned.
