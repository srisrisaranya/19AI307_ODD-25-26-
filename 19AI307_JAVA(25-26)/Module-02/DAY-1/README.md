# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

## AIM:
To Create a class and Objects and print their details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define a class Car with attributes:
brand
model
year
4. Create the first car object (car1).
5. Assign values to car1:
Brand = Toyota
Model = Innova
Year = 2022
6. Create the second car object (car2).
Assign values to car2:
Brand = Hyundai
Model = i20
Year = 2021
7. Display the details of car1.
8. Display the details of car2.
10. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: SARANYA S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:

```
import java.util.*;
class Car{
    String brand;
    String model;
    int year;
}
public class prog {
    public static void main(String[] args) {
        Car car1 = new Car();
        car1.brand = "Toyota";
        car1.model = "Innova";
        car1.year = 2022;

        Car car2 = new Car();
        car2.brand = "Hyundai";
        car2.model = "i20";
        car2.year = 2021;

        System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
        System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
    }
}

```

## OUTPUT:

<img width="782" height="271" alt="image" src="https://github.com/user-attachments/assets/571198fe-cbc1-4191-8b48-f1f4fbfef124" />


## RESULT:
Thus, the java program was executed successfully.
