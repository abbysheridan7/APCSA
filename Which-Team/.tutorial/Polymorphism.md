# Polymorphism

Objects can have more than one type.  The type of the object tells you what methods you can use.  Polymorphic objects can invoke any method from all of their types.

## Example
### Superclass: Sandwich
### Subclasses: GrilledCheese, Italian, IceCream

Objects can have multiple types.  An Italian object is both type Italian and Sandwich becuase an Italian is-a Sandwich.

### New Way to create objects
``` java
Italian sub = new Italian();
Sandwich hoggie = new Italian();
```
The type on the left of the decleration determines what methos can be called.  

sub can call all the Sandwich and Italian methods.

hoggie on the other hand can call all the methods of a Sandwich and any method that is overwritten in Italian.  It CANNOT call any methods unique to Italian.

## Using Polymorphism

Polymorphism is used when you are not sure what subclass will be passed into a method

``` java

public void eatLunch(Sandwich s){
  s.eat();
}
``` java
Italian sub = new Italian();
IceCream cookieSandwich = new IceCream();

eatLunch(sub);
eachLunch(cookieSandwich);
```

Since both Italian and IceCream extend Sandwich they can be passed as an argument.
