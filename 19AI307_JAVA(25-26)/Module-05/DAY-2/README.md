# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:

Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.

## AIM:

To demonstrate serialization and deserialization of Student objects in Java using file handling.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of students n.
4. Create an empty list to store student objects.
Repeat n times:
Read student ID.
Read student name.
Read student marks.
5. Create a Student object and add it to the list.
6. Serialize the list of students and store it in a file (students.dat).
7. Deserialize the student list from the file.
8. Display the deserialized student details.
9. Close the scanner.
10. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); // consume newline
// Write your code here
    for(int i=0;i<n;i++){
        int id=scanner.nextInt();
        scanner.nextLine();
        String name=scanner.nextLine();
        double marks=scanner.nextDouble();
        scanner.nextLine();
        students.add(new Student(id,name,marks));
    }
    String filename="students.dat";
    serializeStudents(students,filename);
    List<Student> deserializedStudents=deserializeStudents(filename);
        
    

        // Display deserialized data
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}

```
## OUTPUT:

<img width="1271" height="497" alt="image" src="https://github.com/user-attachments/assets/cf0422dd-6552-44b4-b414-d2e86fcc11f4" />


## RESULT:
The program successfully serializes the list of student objects into a file and then deserializes them back, displaying the stored student information correctly.
