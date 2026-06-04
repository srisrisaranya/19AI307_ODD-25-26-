# Ex.No:2(B) METHODS

## QUESTION:

Write a method int square(int number) that returns the square of a given number.

## AIM:

To write a java program to write a method int square(int number) that returns the square of a given number.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a number from the user.
4. Create an object of the class.
5. Call the square() method and pass the number as an argument.
6. Calculate the square of the number (number × number).
7. Return the result.
8. Display the result.
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.util.*;
class prog{
    int square(int num){
        return num*num;
    }
public static void main(String[] args){
    Scanner sc=new Scanner(System.in);
    int num=sc.nextInt();
    prog p=new prog();
    int result=p.square(num);
    System.out.print(result);
}
}
```

## OUTPUT:

<img width="701" height="266" alt="image" src="https://github.com/user-attachments/assets/0268f8e4-57e0-446c-bf61-aaaa1d2ac346" />


## RESULT:

Thus,the program for method int square(int number) that returns the square of a given number is executed successfully.
