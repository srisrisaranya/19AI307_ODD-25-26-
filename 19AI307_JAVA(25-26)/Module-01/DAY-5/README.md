# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a Java program to reverse a given string.

## AIM:

To write a java program to reverse a String.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a string from the user.
4. Reverse the string using StringBuilder.
5. Store the reversed string in a variable.
6. Print the reversed string.
7. Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: SARANYA S
RegisterNumber:212223110044  
*/
```

## SOURCE CODE:

```
import java.util.*;
public class main{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        String str=sc.nextLine();
        String rev=new StringBuilder(str).reverse().toString();
        System.out.print("Reversed string: "+rev);
        sc.close();
    }
}
```

## OUTPUT:

<img width="757" height="336" alt="image" src="https://github.com/user-attachments/assets/b4ca11c1-1b29-47b6-83e8-14deae02e998" />


## RESULT:
Thus, the program for reverse a string is executed successfully.
