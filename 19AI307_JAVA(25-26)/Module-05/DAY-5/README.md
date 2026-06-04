# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:

Maintain two int variables a and b, read their initial values from user. Use synchronized block to swap them and print swapped values.

Input:

Two lines: a and b values

Output:

a = <swapped_a>

b = <swapped_b>

## AIM:

To demonstrate synchronization in Java by safely swapping the values of two variables inside a synchronized block.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read two integer values a and b from the user.
4. Enter a synchronized block using a lock object.
5. Store the value of a in a temporary variable.
6. Assign the value of b to a.
7. Assign the temporary value to b.
8. Exit the synchronized block.
9. Display the swapped values of a and b.
10. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    private static final Object lock = new Object();
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = Integer.parseInt(sc.nextLine());
        int b = Integer.parseInt(sc.nextLine());

        synchronized (lock) {
            int temp = a;
            a = b;
            b = temp;
        }

        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}

```
## OUTPUT:

<img width="622" height="412" alt="image" src="https://github.com/user-attachments/assets/e729abfd-4888-49c2-bd6c-f8aeece34851" />


## RESULT:
The program successfully swaps the values of two variables inside a synchronized block and displays the updated values.
