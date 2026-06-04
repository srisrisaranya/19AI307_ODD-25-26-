# Ex.No:5(D) THREAD PRIORITY

## QUESTION:

Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

Note : Read the threadname from the User

set the priority as 4 for t1 and set the priority as 2 for t2

## AIM:

To create and execute multiple threads in Java using the Runnable interface and display their names and priorities.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read two thread names from the user.
4. Create an object of the class implementing Runnable.
5. Create two thread objects with the given names.
Set the priorities of the threads:
Thread 1 priority = 4
Thread 2 priority = 2
6. Start the first thread.
7. Wait for the first thread to finish using join().
8. Start the second thread.
9. Wait for the second thread to finish using join().
10. Display the details of each thread.
11. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.util.*;
public class A implements Runnable{
    public void run(){
        System.out.println(Thread.currentThread());
    }

    public static void main(String[] args) throws InterruptedException{
        Scanner sc=new Scanner(System.in);
        String f=sc.nextLine();
        String s=sc.nextLine();
        A a=new A();
        Thread t1=new Thread(a,f);
        Thread t2=new Thread(a,s);
        t1.setPriority(4);
        t2.setPriority(2);
        t1.start();
        t1.join();
        t2.start();
        t2.join();
    }
}
```
## OUTPUT:

<img width="962" height="342" alt="image" src="https://github.com/user-attachments/assets/1da72250-24cf-47c1-96cb-4000fc529aba" />


## RESULT:
The program successfully creates two threads using the Runnable interface, assigns priorities, executes them sequentially using join(), and displays their details.
