# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:

Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:

Marks ≥ 90: Grade A

Marks ≥ 75 and < 90: Grade B

Marks ≥ 50 and < 75: Grade C

Marks < 50: Grade F

## AIM:

To demonstrate inheritance in Java by creating a Student class that inherits from the Person class and calculates the student's grade based on marks.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the student's name, age, and marks.
4. Create a Student object using the input values.
5. Initialize the inherited attributes (name and age) using the Person constructor.
6. Store the student's marks.
7. Calculate the grade:
Marks ≥ 90 → Grade A
Marks ≥ 75 and < 90 → Grade B
Marks ≥ 50 and < 75 → Grade C
Marks < 50 → Grade F
8. Display the student's name, age, marks, and grade.
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.util.*;
class Person{
 String name;
 int age;
 
 Person(String name,int age){
     this.name=name;
     this.age=age;
 }
}
class Student extends Person{
    int marks;
    Student(String name,int age,int marks){
        super(name,age);
        this.marks=marks;
    }
    String calgrade(){
        if(marks>=90) return "A";
        else if(marks>=75 && marks<90) return "B";
        else if(marks>=50&&marks<75) return "C";
        else return "F";
    }
}
public class main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        String name=sc.next();
        int age=sc.nextInt();
        int marks=sc.nextInt();
        Student s=new Student(name,age,marks);
        System.out.println("Name: "+s.name);
         System.out.println("Age: "+s.age);
         System.out.println("Marks: "+s.marks);
         System.out.println("Grade: "+s.calgrade());
    }
}

```
## OUTPUT:

<img width="761" height="677" alt="image" src="https://github.com/user-attachments/assets/2ee654f8-a803-4e37-afd1-34aaff8f8a65" />


## RESULT:
The program successfully demonstrates inheritance by extending the Person class into a Student class and displays the student's details along with the calculated grade.
