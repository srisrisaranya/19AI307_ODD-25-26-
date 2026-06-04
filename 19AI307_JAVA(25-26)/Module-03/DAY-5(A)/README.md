# Ex.No:3(E) INNER CLASS

## QUESTION:

 Write a Java program where the inner class is declared private and accessed through a method in the outer class. 

## AIM:

To demonstrate the use of a private inner class in Java and access it through a method of the outer class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read an integer value from the user.
4. Create an object of the outer class.
5. Call the accessinner() method and pass the input value.
6. Inside accessinner(), create an object of the private inner class.
7. Call the display() method of the inner class.
8. Display the input value.
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.util.*;
public class outerc{
    private class innerc{
        public void display(int data){
            System.out.println("Data set inside private inner class: "+data);
        }
    }
    public void accessinner(int data){
        innerc inner=new innerc();
        inner.display(data);
    }
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        if(sc.hasNextInt()){
            int inputdata=sc.nextInt();
            outerc outer=new outerc();
            outer.accessinner(inputdata);
        }
    }
}
```

## OUTPUT:

<img width="1062" height="365" alt="image" src="https://github.com/user-attachments/assets/ba78b134-2803-4f7d-9abe-155e9a01ffe7" />


## RESULT:
The program successfully demonstrates the use of a private inner class by accessing its method through the outer class and displaying the given data.
