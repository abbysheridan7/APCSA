# User Input

A scanner is used to get input in the console

## Initialize a Scanner
At the top of your file before the class header
```
import java.util.Scanner;
```
In the main method/other method
```
// Creates a Scanner object
Scanner input = new Scanner(System.in);
```
## Reading Inputs
```
// Reads a String
String str = input.nextLine();

//Reads an integer
int age = input.nextInt();

//Reads a double
double gpa = input.nextDouble();

//Reads a boolean
boolean isTired = input.nextBoolean();
```
Prompt the user with a System.out.print()/System.out.println() before you get the input
```
// Ask user for input
System.out.println("What is your age?");
int age = input.nextInt();
```
