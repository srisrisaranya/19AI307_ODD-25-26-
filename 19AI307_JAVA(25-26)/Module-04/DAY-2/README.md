# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:

In a gaming lounge, there is only one master console power switch that controls all gaming consoles. Whenever a player turns on any console, it internally triggers the master power. The master switch must ensure only one instance is ever created, regardless of how many times it's accessed, to prevent power fluctuations.

Every time a player accesses the master switch, it logs an access count. Since the switch is Singleton, the count should increment globally and reflect shared state.

Input Format:

n
[Player1]
[Player2]
...
First line: Integer n – number of players turning on consoles

Next n lines: Each line contains the player's name.

 

Output Format:
For each player, print:

[PlayerName] accessed Master Power Switch. Total accesses so far: [count]

## AIM:

To demonstrate the Singleton Design Pattern in Java by allowing multiple users to access a single MasterPowerSwitch object and tracking the number of accesses.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare a static object reference and an access counter.
4. Make the constructor private to prevent object creation from outside the class.
5. Create a getInstance() method:
6. If no object exists, create one.
7. Return the same object for all requests.
8. Read the number of users n.
9. Repeat n times:
10. Read the player's name.
11. Get the singleton instance using getInstance().
12. Increment the access counter using logAccess().
13. Display the player's name and the total access count.
14. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.util.*;
class MasterPowerSwitch {
    //Type your code 
    private static MasterPowerSwitch instance;
    private int accessCount;
    private MasterPowerSwitch() {
        accessCount = 0;
    }
    public static MasterPowerSwitch getInstance() {
        if (instance == null) {
            instance = new MasterPowerSwitch();
        }
        return instance;
    }
    public int logAccess() {
        accessCount++;
        return accessCount;
    }
}
public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String player = sc.nextLine();
            MasterPowerSwitch power = MasterPowerSwitch.getInstance();
            int count = power.logAccess();
            System.out.println(player + " accessed Master Power Switch. Total accesses so far: " + count);
        }
    }
}

```
## OUTPUT:

<img width="1302" height="365" alt="image" src="https://github.com/user-attachments/assets/5a2bd740-e273-4785-8929-329f26c51e0a" />


## RESULT:
The program successfully implements the Singleton Design Pattern, ensuring that only one MasterPowerSwitch object exists and accurately tracks the total number of accesses by different users.
