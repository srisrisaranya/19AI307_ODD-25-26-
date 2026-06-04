# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types

## AIM:

To demonstrate the Abstract Factory Design Pattern in Java by creating UI components (Button and Checkbox) for different themes.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the theme (dark or light) from the user.
4. If the theme is dark:
5. Create a DarkThemeFactory object.
6. Else if the theme is light:
7. Create a LightThemeFactory object.
8. Otherwise, display "Invalid theme" and stop.
9. Use the factory to create a Button and a Checkbox.
10. Call the render() method for both components.
11. Display the corresponding theme-based components.
12. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
interface Button {
    void render();
}
interface Checkbox {
    void render();
}
class DarkButton implements Button {
    public void render() {
        System.out.println("Dark Button created");
    }
}
class LightButton implements Button {
    public void render() {
        System.out.println("Light Button created");
    }
}
class DarkCheckbox implements Checkbox {
    public void render() {
        System.out.println("Dark Checkbox created");
    }
}
class LightCheckbox implements Checkbox {
    public void render() {
        System.out.println("Light Checkbox created");
    }
}
interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}
class DarkThemeFactory implements UIFactory {
    public Button createButton() {
        return new DarkButton();
    }
public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}
class LightThemeFactory implements UIFactory {
    public Button createButton() {
        return new LightButton();
    }
    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String theme = scanner.nextLine().toLowerCase();
        UIFactory factory;
        if (theme.equals("dark")) {
            factory = new DarkThemeFactory();
        } else if (theme.equals("light")) {
            factory = new LightThemeFactory();
        } else {
            System.out.println("Invalid theme");
            return;
        }

        factory.createButton().render();
        factory.createCheckbox().render();
    }
}

```
## OUTPUT:

<img width="801" height="397" alt="image" src="https://github.com/user-attachments/assets/ce74d5e8-dea2-47b7-8739-f9314c878715" />


## RESULT:
The program successfully demonstrates the Abstract Factory Design Pattern by creating and displaying theme-specific UI components (Button and Checkbox) based on the user's selected theme.
