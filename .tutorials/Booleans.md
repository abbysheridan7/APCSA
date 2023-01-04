# Booleans
A boolean holds/evaluates to true or false

### Creating and intializing a boolean
```
boolean isHappy = true;
```

### Getting a boolean input
```
System.out.println("Is it raining outside?");
booean isRaining = input.nextBoolean();
```

### Not Operator
Gets the opposite value of the boolean
```
boolean x = !y
```

### And Operator
Both sides of the And need to be true inorder for it to evaluate to true
```
boolean goodDay = isSunny && isHot;
```

### Or Operator
Atleast ome side of the Or needs to be true for it to evaluate to true
```
boolean badDay = isRaining || isCold;
```

### Combining Booleans
Order of Operations
* Not !
* And &&
* Of ||


## Truth Tables
### And Table
| x | y | x && y |
|---|---|--------|
|true | true | true |
|true | false| false|
|false| true | false|
|false| false| false|

### Or Table
| x | y |x &#124;&#124; y|
|---|---|--------|
|true | true | true |
|true | false| true |
|false| true | true |
|false| false| false|
