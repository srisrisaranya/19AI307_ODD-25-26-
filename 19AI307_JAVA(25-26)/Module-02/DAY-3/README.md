# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:

Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

## AIM:

To create a Smartphone class using encapsulation and increase its storage capacity using methods.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Smartphone object.
4. Read the brand, model, and storage capacity from the user.
5. Set these values using setter methods.
6. Read the additional storage value.
7. Increase the storage capacity using the increaseStorage() method.
8. Display the updated smartphone details.
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Smartphone {
    private String brand;
    private String model;
    private int storageCapacity;

    
    public String getBrand() {
        return brand;
    }

    public String getModel() {
        return model;
    }

    public int getStorageCapacity() {
        return storageCapacity;
    }

    
    public void setBrand(String brand) {
        this.brand = brand;
    }

    public void setModel(String model) {
        this.model = model;
    }

    public void setStorageCapacity(int storageCapacity) {
        this.storageCapacity = storageCapacity;
    }

   
    public void increaseStorage(int value) {
        if (value > 0) {
            this.storageCapacity += value;
        }
    }

    
    public void display() {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
        System.out.println("------------------------------");
    }
}

//continue your code here
public class main{
public static void main(String[] args){
    Scanner sc=new Scanner(System.in);
    Smartphone s=new Smartphone();
    s.setBrand(sc.nextLine());
    s.setModel(sc.nextLine());
    s.setStorageCapacity(sc.nextInt());
    int extra=sc.nextInt();
    s.increaseStorage(extra);
    s.display();
}
}
```
## OUTPUT:

<img width="1037" height="537" alt="image" src="https://github.com/user-attachments/assets/dac0f5b1-a323-43c4-b13b-9a35c7b6d012" />

## RESULT:

The program successfully stores smartphone details using setter methods, increases the storage capacity, and displays the updated information.
