# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely has just started learning Java and is very excited about how to display messages on the screen. Her first mission is to understand how different types of print statements work:

System.out.print() → prints on the same line

System.out.println() → prints and moves to the next line

System.out.printf() → prints formatted output


## AIM:
To write a Java program that demonstrates the use of variables, data types, operators, and different print statements (print, println, and printf).

## ALGORITHM :
1.	Start the program.
2.	Import the required package java.util.* (optional).
3.	Declare variables of different data types (int, float, char, String).
4.	Perform simple arithmetic operations using operators.
5.	Use System.out.print() to display output on the same line.
6.	Use System.out.println() to display output on the next line.
7.	Use System.out.printf() to print formatted output.
8.	End the program.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: SARANYA S
Register Number:212223110044
*/
```

## Sourcecode.java:
```
import java.util.*;
public class main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        System.out.println("Initial countdown = "+a);
        int post=a--;
        System.out.println("After post-decrement (a--) = "+post+", Now a = "+a);
        int pre=--a;
        
        
        System.out.println("After pre-decrement (--a) = "+pre+", Now a = "+a);
        sc.close();
    }
}
```

## OUTPUT:

<img width="982" height="382" alt="image" src="https://github.com/user-attachments/assets/b4845509-a948-42a7-9576-c2e9f83970b0" />

## RESULT:
Thus, the Java program demonstrating variables, data types, operators, and print statements was successfully executed.





