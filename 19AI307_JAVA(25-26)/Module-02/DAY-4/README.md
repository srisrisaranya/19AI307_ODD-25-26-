# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:

Write a Java program with one instance variable and access it from a method.

## AIM:

To illustrate the use of a static variable and a static method in Java.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read an integer value from the user.
4. Call the static method setValue() and pass the input value.
5. Store the value in the static variable.
6. Display the value of the static variable.
7. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by:Saranya S
RegisterNumber: 212223110044
*/
```

## SOURCE CODE:
```
import java.util.*;
class prog{
    static int value;
    static void setValue(int val){
        value=val;
    }
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        prog p=new prog();
        prog.setValue(n);
        System.out.println("The value of the instance variable is: "+p.value);
    }
}
```
## OUTPUT:

<img width="1025" height="320" alt="image" src="https://github.com/user-attachments/assets/ae717313-5d3c-4d78-badf-f36a0c302a43" />

## RESULT:

The program successfully stores the user-entered value in a static variable using a static method and displays it on the screen.
