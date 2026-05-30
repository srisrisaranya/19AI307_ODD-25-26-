# Ex.No:1(D) ARRAYS

## QUESTION:

Write a Java program to reverse an array

## AIM:
To write a java program to reverse an array.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the size of the array n.
4. Create an array arr of size n.
5. Read n elements and store them in the array.
6. Traverse the array from the last index (n - 1) to the first index (0).
7. Print each element while traversing.
8. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: SARANYA S
RegisterNumber: 212223110044 
*/
```

## SOURCE CODE:
```
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        for (int i = n - 1; i >= 0; i--) {
            System.out.print(arr[i] + " ");
        }
    }
}

```
## OUTPUT:

<img width="592" height="620" alt="image" src="https://github.com/user-attachments/assets/62580c25-199c-4d65-9a9d-5d072ccf4b31" />


## RESULT:

Thus the java code for reverse an array is executed successfully.
