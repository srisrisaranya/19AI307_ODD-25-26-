# Ex.No:3(D)    INTERFACE 

## QUESTION:

You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.


 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".

Input:

temperature
botType (1 for SunBot, 2 for RainBot)Output:
Prediction as a string.

## AIM:


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the temperature from the user.
4. Read the bot type from the user.
5. If the bot type is 1, create a SunnyBot object.
6. Otherwise, create a RainyBot object.
Call the forecast() method:
For SunnyBot:
If temperature > 30, return "HOT".
Otherwise, return "MODERATE".
7. For RainyBot:
If temperature < 20, return "COLD".
Otherwise, return "WARM".
8. Display the forecast result.
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Saranya S
RegisterNumber:  212223110044
*/
```

## SOURCE CODE:
```
import java.util.*;

interface WeatherBot {
    String forecast(int temperature);
}

class SunnyBot implements WeatherBot {
    public String forecast(int temperature) {
        return temperature > 30 ? "HOT" : "MODERATE";
    }
}

class RainyBot implements WeatherBot {
    public String forecast(int temperature) {
        return temperature < 20 ? "COLD" : "WARM";
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int temp = sc.nextInt();
        int type = sc.nextInt();
        WeatherBot bot;

        if (type == 1)
            bot = new SunnyBot();
        else
            bot = new RainyBot();

        System.out.println(bot.forecast(temp));
    }
}

```
## OUTPUT:

<img width="665" height="267" alt="image" src="https://github.com/user-attachments/assets/05a3385e-242c-4c53-9dae-63634c2cd476" />


## RESULT:
The program successfully demonstrates interface implementation by generating weather forecasts using different bot classes based on the user's choice.
