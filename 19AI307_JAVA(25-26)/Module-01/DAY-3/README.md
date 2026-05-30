# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

Write a Java program that asks the user to enter how many terms of the Fibonacci series they want to display.
Use a for loop to generate the series.
The first two terms should always be 0 and 1.
From the third term onwards, each term should be calculated as the sum of the previous two terms.
Display the series in a clear and readable format.

## AIM:

To write a java program for Fibonacci series.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number n from the user.
Initialize:
a = 0
b = 1
4.Print the first two Fibonacci numbers (0 and 1).
5.Repeat from i = 2 to n - 1:
Calculate c = a + b.
Print c.
Assign a = b.
Assign b = c.
6.Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: SARANYA S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.util.*;
public class main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int a=0,b=1,c;
        System.out.print("Fibonacci Series: "+a+" "+b);
        for(int i=2;i<n;i++){
            c=a+b;
            a=b;
            b=c;
        System.out.print(" "+c);
        }
    }
}
```

## OUTPUT:
<img width="822" height="311" alt="image" src="https://github.com/user-attachments/assets/4565f983-5d1b-499d-a4a1-a42fbf2fa84b" />

## RESULT:
Thus,the java program for fibonacci series is executed successfully.
