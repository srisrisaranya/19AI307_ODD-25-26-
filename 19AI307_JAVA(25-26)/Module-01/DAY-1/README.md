# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:

Lovely wants to enter a secure tech conference. The security system checks certain conditions to grant access. These conditions are:

She must be registered (true/false).

She must have a valid ID (true/false).

She must NOT be blacklisted (true/false).

The system uses logical operators to evaluate her access eligibility:

If she is registered AND has a valid ID, and NOT blacklisted, she is granted access.

Otherwise, access is denied.

Your task is to evaluate these conditions using logical operators and print whether access is granted or denied.


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
    public static void main(String[] arg)
    {
        Scanner sc=new Scanner(System.in);
        boolean r=sc.nextBoolean();
        boolean v=sc.nextBoolean();
        boolean b=sc.nextBoolean();
        boolean res=((r&&v)&&!b);
        System.out.println("Access Granted: "+res);
        sc.close();
    }
}
```

## OUTPUT:

<img width="982" height="382" alt="image" src="https://github.com/user-attachments/assets/b4845509-a948-42a7-9576-c2e9f83970b0" />

## RESULT:
Thus, the Java program demonstrating variables, data types, operators, and print statements was successfully executed.





