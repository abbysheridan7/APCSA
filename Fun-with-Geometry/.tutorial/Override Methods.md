# Override Methods

Subclasses can override the methods of a superclass.  Sometime a subclass has a method of the same name but does something a bit different than the superclass.

SeaMonster uses overwritting to change the <code>moveX </code> method to fit a SeaMonster.  When a method is overwritten the method in the superclass is ignored.

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

  @Override
  public void moveX(int howFar){
    swimX(howFar * 3);
  }
}
```


