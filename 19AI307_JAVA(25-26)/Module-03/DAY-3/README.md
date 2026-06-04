# Ex.No:3(C) ABSTRACTION

## QUESTION:

Create an abstract class DiceGame with method play().
Two subclasses:

TwoDiceGame: Rolls 2 dice, winner is player with higher total

OneDiceDouble: Each player rolls 1 die twice, if both dice are same, player gets bonus 10 points

Input Format:

First line: 1 or 2
Second line (for each player): 2 dice values for each player

Output Format:
Player 1 wins / Player 2 wins / Draw
Second line (for each player): 2 dice values for each player

## AIM:

To demonstrate abstraction in Java by implementing different dice game rules using an abstract class and method overriding.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the game type from the user.
4. Read the dice values for Player 1 and Player 2.
If game type is 1:
Calculate the sum of both dice for each player.
Compare the sums and determine the winner.
If game type is 2:
5. Calculate the sum of both dice for each player.
6. Add 10 bonus points if a player rolls a double.
7. Compare the scores and determine the winner.
8. If the game type is invalid, display an error message.
9. Display the result (Player 1 wins, Player 2 wins, or Draw).
10. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
abstract class DiceGame {
    public abstract String play(int[] p1, int[] p2);
}
class TwoDiceGame extends DiceGame {
    @Override
    public String play(int[] p1, int[] p2) {
        int sum1 = p1[0] + p1[1];
        int sum2 = p2[0] + p2[1];

        if (sum1 > sum2) return "Player 1 wins";
        else if (sum2 > sum1) return "Player 2 wins";
        else return "Draw";
    }
}
class OneDiceDouble extends DiceGame {
    @Override
    public String play(int[] p1, int[] p2) {
        int score1 = p1[0] + p1[1];
        int score2 = p2[0] + p2[1];

        if (p1[0] == p1[1]) score1 += 10;
        if (p2[0] == p2[1]) score2 += 10;

        if (score1 > score2) return "Player 1 wins";
        else if (score2 > score1) return "Player 2 wins";
        else return "Draw";
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int gameType = sc.nextInt();

        int[] p1 = new int[2];
        int[] p2 = new int[2];

        p1[0] = sc.nextInt();
        p1[1] = sc.nextInt();
        p2[0] = sc.nextInt();
        p2[1] = sc.nextInt();

        DiceGame game;
        if (gameType == 1) {
            game = new TwoDiceGame();
        } else if (gameType == 2) {
            game = new OneDiceDouble();
        } else {
            System.out.println("Invalid game type");
            sc.close();
            return;
        }

        System.out.println(game.play(p1, p2));
        sc.close();
    }
}
```
## OUTPUT:

<img width="812" height="401" alt="image" src="https://github.com/user-attachments/assets/3d2d2ee2-c46f-43e8-bbc7-0e5d06a8bc30" />


## RESULT:
The program successfully demonstrates abstraction and method overriding by implementing different dice game rules and determining the winner based on the selected game type.
