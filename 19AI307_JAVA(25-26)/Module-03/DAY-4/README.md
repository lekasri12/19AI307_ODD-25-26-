# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.

Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".

## AIM:
To implement weather prediction using interfaces with two bots — SunBot and RainBot.

## ALGORITHM :
1.	Create WeatherBot interface with predict() method.
2.	Implement SunBot and RainBot classes with different prediction logic.
3.	Take temperature and botType as input.
4.	Use the chosen bot to call predict().
5.	Display the prediction.

## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
interface WeatherBot {
    String predict(int temperature);
}
class SunBot implements WeatherBot {
    @Override
    public String predict(int temperature) {
        if (temperature > 30) {
            return "HOT";
        } else {
            return "MODERATE";
        }
    }
}
class RainBot implements WeatherBot {
    @Override
    public String predict(int temperature) {
        if (temperature < 20) {
            return "COLD";
        } else {
            return "WARM";
        }
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int temperature = sc.nextInt();   
        int botType = sc.nextInt();       
        WeatherBot bot;
        if (botType == 1) {
            bot = new SunBot();
        } else {
            bot = new RainBot();
        }
        System.out.println(bot.predict(temperature));
    }
}

```

## OUTPUT:

<img width="327" height="158" alt="image" src="https://github.com/user-attachments/assets/65f8a872-471f-4b1a-9448-0a749da283cf" />


## RESULT:
Thus, the program predicts weather conditions using interface implementation and method overriding.


