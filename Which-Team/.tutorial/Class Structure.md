# Class Structure

##This is an example of a class called 
``` java
// class header
public class Robot {

// instance variables
// should be private
private double x;
private double y;
private String name;

//default constructor
public Robot(){
  x = 90;
  y = 100;
  name = "";
}

//constructor with arguments
public Robot(int x, int y, String n){
  this.x = x;
  this.y = y;
  name = n;
}

// setter methods
// these methods are of type void

public void setPostion(int x, int y){
  this.x = x;
  this.y = y;
}

public void setName(String name){
  this.name = name;
}

// getter methods
// these methods are the type that they are returning

public double getX(){
  return x;
}

public double getY(){
  return y;
}

public String getName(){
  return name;
}

// toString method
// returns a description of the object

public String toString(){
  return "The robot " + getName() + " is located at (" + getX() + " , "" getY() +");
}

}
```
