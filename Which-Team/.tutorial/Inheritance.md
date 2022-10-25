# Is-A Relationship

Inheritance is when a class acquired the instance variables and methods of another class.  This allows up to create a hierarchy of objects that share methods and states.

When you create a subclass is aquires all the instance variables of the superclass.  You can access the instance variables with your getters. <code>super.methodName()</code>

The subclass can do everything the superclass can do plus it can use its own methods.  
``` java
SeaMonster stan = new SeaMonster();
stan.dive(7); //SeaMonster method
stan.changeDirection(3); //Monster method
```
Stan can dive and swimX because he is a SeaMonster.  Stan is also able to changeDirection, moveX and moveY because a SeaMonster is-a Monster.  

## Superclass
``` java
public class Monster {

  // instance variables that all monsters share
  private String name;
  private int direction;
  private int x;
  private int y;

  //constructor
  public Monster(String name, int direction, int x, int y){
    this.name = name;
    this.direction = direction;
    this.x = x;
    this.y = y;
  }

  public void moveX(int howFar){
    x += howFar;
  }

  public void moveY(int howFar){
    y += howFar;
  }

  public void changeDirection(int d){
    direction = d;
  }
}
```
## Subclass
``` java
public class SeaMonster {
  //instance variable unique to a seaMonster
  private int depth;

  //default constructor
  // set instance variables of a sea monster and 
  //passes information to set Monster instance variables
  //make sure your super call goes first
  public SeaMonster(){
    super(0, 0, "unknown");
    depth = 0;
  }
  
  //constructor
  // set instance variables of a sea monster and 
  //passes information to set Monster instance variables
  //make sure your super call goes first
  public SeaMonster(int x, int y, int direction, int depth, String name){
    super(x, y, name);
    this.depth = depth;
  }

  public void dive(int howFar){
    depth += howFar;
  }

  public void swimX(int distance){
    moveX(distance);
  }
}
```


