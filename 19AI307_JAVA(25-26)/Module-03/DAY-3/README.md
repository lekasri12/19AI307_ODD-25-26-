# Ex.No:3(C) ABSTRACTION

## QUESTION:
Description:
Create abstract class GameScore with method finalScore().
Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

## AIM:
To write a Java program using an abstract class GameScore with subclasses ArcadeGame and PuzzleGame, each implementing its own finalScore() method.

## ALGORITHM :
1.	Create an abstract class GameScore with an abstract method finalScore().
2.	Define subclass ArcadeGame where finalScore = baseScore + (level × 100).
3.	Define subclass PuzzleGame where
4.	If attempts ≤ 3, score = 1000 - (attempts × 100)
5.	Else score = 500.
6.	Take user input for game type and relevant values.
7.	Display the final score based on game type.

## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: LEKASRI G
RegisterNumber: 212223100025
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

abstract class GameScore {
    abstract int finalScore();
}
class ArcadeGame extends GameScore {
    int base, level;

    ArcadeGame(int base, int level) {
        this.base = base;
        this.level = level;
    }

    @Override
    int finalScore() {
        return base + (level * 100);
    }
}
class PuzzleGame extends GameScore {
    int attempts;

    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }

    @Override
    int finalScore() {
        if (attempts <= 3) {
            return 1000 - (attempts * 100);
        } else {
            return 500;
        }
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int choice = sc.nextInt();
        GameScore game;
        if (choice == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();
            game = new ArcadeGame(base, level);
        } else {
            int attempts = sc.nextInt();
            game = new PuzzleGame(attempts);
        }
        System.out.println(game.finalScore());
    }
}

```

## OUTPUT:

<img width="380" height="207" alt="image" src="https://github.com/user-attachments/assets/2e026245-f236-4133-81e5-14ac104ca8c2" />


## RESULT:
Thus, the program successfully demonstrates abstraction and inheritance by computing the final score for different game types using subclass-specific logic.



