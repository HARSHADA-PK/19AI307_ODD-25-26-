# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class GameScore with method finalScore().  
Subclasses:
ArcadeGame: score = baseScore + (level × 100)
PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

## AIM:
To write a Java program that uses an abstract class to calculate final game scores for two types of games:  
ArcadeGame and PuzzleGame, each implementing its own scoring logic.

## ALGORITHM:
1. Create an abstract class `GameScore` with the abstract method `finalScore()`.
2. Create subclass `ArcadeGame` with:
   - Attributes: `base`, `level`
   - Scoring rule: `finalScore = base + (level × 100)`
3. Create subclass `PuzzleGame` with:
   - Attribute: `attempts`
   - Scoring rule:
     - If attempts ≤ 3 → `finalScore = 1000 - (attempts × 100)`
     - Else → `finalScore = 500`
4. In the `main` method:
   - Read `type` (1 for ArcadeGame, 2 for PuzzleGame)
   - If `type == 1`:
     - Read `base` and `level`
     - Create `ArcadeGame` object
   - Else:
     - Read `attempts`
     - Create `PuzzleGame` object
   - Call `finalScore()` and print the result.
5. End the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Harshada P K
RegisterNumber:  212224060097
*/
```

## SOURCE CODE:
```
import java.util.*;
abstract class Game
{
    abstract int finalScore();
}
class Arcade extends Game
{
    int base;
    int level;
    Arcade(int base,int level)
    {
        this.base=base;
        this.level=level;
    }
    int finalScore()
    {
        return base+(level*100);
    }
}
class Puzzle extends Game
{
    int att;
    Puzzle(int att)
    {
        this.att=att;
    }
    int finalScore()
    {
        return (att<=3)?1000-(att*100):500;
    }
}
public class main
{
    public static void main(String[] args)
    {
        Scanner input=new Scanner(System.in);
        int type=input.nextInt();
        if(type==1)
        {
            int base=input.nextInt();
            int level=input.nextInt();
            Arcade a=new Arcade(base,level);
            System.out.println(a.finalScore());
        }
        else if(type==2)
        {
            int att=input.nextInt();
            Puzzle p=new Puzzle(att);
            System.out.println(p.finalScore());
        }
    }
}
```

## OUTPUT:
<img width="354" height="206" alt="image" src="https://github.com/user-attachments/assets/c7d29ada-3636-4732-847f-28a95ba50bc8" />

## RESULT:
The program successfully calculates and displays the final score based on game type and user input using abstract methods and dynamic method dispatch.


