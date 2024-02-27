# OBSIDIAN JAVA SUMMARY
Summary was created in Obsidian while using JetBrains Academy and learning for university.

## Basic

WORA principle - Write Once Run Anywhere


### Literals

Integer Numbers: ``1,2,3,4,1000``
``100_000_000 = 100000000 -- better readability``

Single Characters: ``'A' 'B' 'C'`` single quotes, can only contain single characters, numbers or symbols.

String: ``"Double quotes are used for strings"``, ``"0"`` is also correct! not to be confused with `'0'`!


## Terminology

- Program - a sequence of instructions (called statements), which are executed one after another in a predictable manner. Sequential flow is the most common and straight foreward sequence of statements, in which statements are executed in the order that they are written - from top to bottom in a sequential manner.
- Statement - a single action (like print a text) terminated by semi-colon; .
- Block - a group of zero, one or more statements enclosed by a pair of braces {...}.
- Method - a sequence of statements that represents a high-level operation (also known as subprogram or procedure).
- Syntax - a of rules that define how a program needs to be written in order to be valid; Java has its own specific syntax.
- Keyword - a word that has a special meaning in the programming language ``public, class, ...``. These words cannot be used as variable names for your own program.
- Identifier or name - a word that refers to something in a program (such as a variable or a function name).
- Comment - a textual explanation of what the code does. Java comments start with ``//``.
- Whitespace - all characters that are not visible (space, tab, newline, etc.)
- Word - piece of text surrounded by whitespace (token).
- Constructor - Method with no return type -- capital first letter, same name as the class.
- Void - no return value
- Definition at class level - can be used at all specific methods.
- Definition at local data - can be used in the data level -- in the specific method.
- Actual parameters - input for invoking a method.
- Formal parameters - defined in the method.
- Visibility modifiers - ``final`` define constants; ``public`` can be referenced anywhere; ``protected`` not visible outside the package ``private`` can only be referenced within the class

<div style="page-break-after: always;"></div>

## Comments

- ``//`` everything after until the end of the line is comment, not read as code.
- ``/* .....*/`` everything between is read as comment, also multiline.
- don't use unnecessary comments -- clean code.
- some well placed "tactical" comments can be very useful.
```java
/**
* This is a javadoc comment.
*/
```


## Variables


- ``DataType variableName`` = initialisation. 
- The type or data type determines what possible operations can be performed on the variable and which values can be stored in it.
- The name or identifier distinguishes the variable from others.
- The assignment operator denoted as ``=`` is used to assign a single value to a variable.
- The initialisation is a value or a result of an expression that is assigned to the variable.


## Naming Variables

- Names are case-sensitive.
- A name can include Unicode letters, digits and two special characters ``$ and _``.
- A name cannot start with a digit.
- A name must not be a keyword ``class, static, int`` are illegal names.
- A variable with a good name can provide an explanation for complicated code without using a comment.

<div style="page-break-after: always;"></div>

## Conventions for naming variables (optional)

- If a variable name is a single word, it should be in lowercase ``number, price``.
- If a variable name includes multiple words, it should be in ``lowerCamelCase``.
- Variable names should not start with ``_`` and ``$`` characters, although they are allowed.
- Choose a name that makes sense, e.g. ``score`` makes more sense than ``s``, although they are both valid.


## Modifiers

``final double CM_PER_INCH = 2.54`` - value cannot be changed anymore, written in capital letters.


## Data Types

- There are 8 different data types.
- Wrapper classes e.g. Integer for int, treats primitive int as an object reference.


## Scanning input

- Standart class: Scanner - to use this class, import ``java.util.Scanner``.
- After import add construction ``Scanner scan = new Scanner(System.in)``. - with this line, object of scanner class is created, enabling to use its methods.

```java
Scanner scan = new Scanner(System.in);
String name = scanner.next();
System.out.println("Hello, " + name + "!");
```

- After invoking ``next()`` or ``nextLine()`` method, input is stored as variable. ``next()`` reads input until next whitespace and ``nextLine()`` reads input until end of the line.
- After Scanning `nextInt()`, the end of the line is not read. Insert `nextLine()`to read end of line.
- ``scanner.close()`` - Close scanner class after finished scanning.


## Arithmetic Operations

- ``+`` addition  
- ``-`` subtraction 
- ``*`` multiplication
- ``/`` integer division
- ``%`` remainder


## Integer Types

- ``int number = 25`` - 25 is the integer number stored as int
- ``long secondNumber = 15L`` 15L is the long number stored. Use upper case L because lower case looks similar to I and 1.
- ``n = n + 4`` equals to ``n += 4`` -- 14
- ``*=``
- ``%=``
- ``/=``


## Increment and Decrement

```java
n = 10;
n++; // value is now 11
n--; // value is now 9
```

- prefix ``++n`` or ``--n`` increases/decreases the value before it is used.
- postfix ``n++`` or ``n--`` increases/decreases the value after it is used.

<div style="page-break-after: always;"></div>

## Characters

- Unicode (UTF-16) - encoding table for characters (https://unicode-table.com/en)
- char type stores a lot of characters. Latin, numbers, Symbols.
- Every Character has hexadecimal value assigned to it, in "ascending" order (also a regular number assigned to it).
- t can be incremented or decremented, assigned codes can be added, subtracted, etc.



## Escape sequences

- ``\n`` is the newline character.
- ``\t`` is the tab character.
- ``\r`` is the carriage return character.
- ``\\`` is the backslash character itself.
- ``\'`` is the single quote mark.
- ``\"`` is the double quote mark.


## Strings

- **immutable type** - it's not possible to change a character in a string.
- It has methods for getting individual characters and extracting substrings.
- Individual characters can be accessed by indexes, the first character has the index 0, the last one - the length of the string-1.
- Non-primitive type.




### Methods of a String

- ``lenght()`` returns the number of characters of a string.
- ``charAt(int index)`` returns character at its index.
- ``isEmpty()`` returns true if the string is empty, otherwise false.

```java
// Concatenate two strings using the + operator
String str1 = "Hello, ";
String str2 = "world!";
String str3 = str1 + str2;
System.out.println(str3); // Output: "Hello, world!"

// Find the length of a string
String str4 = "Hello, world!";
int length = str4.length();
System.out.println(length); // Output: 13

// Extract a substring from a string
String str5 = "Hello, world!";
String substring = str5.substring(7, 12);
System.out.println(substring); // Output: "world"

// Replace characters in a string
String str6 = "Hello, world!";
String replaced = str6.replace("world", "Java");
System.out.println(replaced); // Output: "Hello, Java!"

// Convert a string to uppercase or lowercase
String str7 = "Hello, world!";
String upper = str7.toUpperCase();
System.out.println(upper); // Output: "HELLO, WORLD!"
String lower = str7.toLowerCase();
System.out.println(lower); // Output: "hello, world!"

// Check if a string starts or ends with a certain character or substring
String str8 = "Hello, world!";
boolean startsWithH = str8.startsWith("H");
System.out.println(startsWithH); // Output: true
boolean endsWithBang = str8.endsWith("!");
System.out.println(endsWithBang); // Output: true
```


## Boolean and Logical Operators

Boolean is a data type with 2 possible values, true or false.
Java has 4 logical operators:
- **NOT** - denoted as ! - reverses the boolean value.
- **AND** - denoted as && - returns true if both operands are true.
- **OR** - denoted as || - returns true if at least one operand is true.
- **XOR** - denoted as ^ - returns true if operands are different.

**! (NOT); ^(XOR); &&(AND); || (OR)** is the order of priorities.

- ``boolean b = true || !false`` true, because !false is evaluated first (before ||).
- short circuit evaluation: means &&, or || don't need to evaluate second argument, when first argument from && is false, does not matter second, it is always false.
- In || if the first argument is true, the second does not matter, it is always true.

<div style="page-break-after: always;"></div>

## Relational Operators

``==`` equal to
``!=`` not equal to
``>`` greater than
``>=`` greater than or equal
``<`` less than
``<=`` less than or equal


## Narrow Typecasting
``char specialChar = (char) (r.nextInt(4) + 35);``
New type must be in parentheses in front of value.

## Conditional Statements
`if` `else` = Keywords

```java
if (num % 2 == 0) {
    System.out.println("It's an even number");
} else {
    System.out.println("It's an odd number");
}
```

```java
if (dollars < 1000) {
    System.out.println("Buy a laptop");
} else if (dollars < 2000) {
    System.out.println("Buy a personal computer");
} else {
    System.out.println("Buy a data center or a quantum computer");
}
```

**Ternary operator:**

condition ? true_case : else_case; *General Syntax*
``System.out.println(num % 2 == 0 ? "even" : "odd");``

## Loops

- For Loop:
```java
int n = 9;
for (int i = 0; int i <= n; i++) {
    System.out.print(i + " ");
}
```
- if variable defined outside of loop.
- code displays - 0 1 2 3 4 5 6 7 8 9

- For-Each Loop (Enhanced For Loop):
```java
// Enhanced for loop example
int[] numbers = {1, 2, 3, 4, 5};

// loop through the array and print each element
for (int number : numbers) {
    System.out.println(number);
}

// Output: 1 2 3 4 5
```

 


## While and Do-While Loop

```java
while (condition) {
    // body: do something repetitive
}
```
- condition is checked first, if true, body executed as long as true.
- in the condition, methods can be invoked: as .hasNext() method of Scanner class.
- .hasNext() returns true if next element exists and false if not.

```java
do {
    //body: do something
} while (condition);
```
- condition is checked after first execution, if still true, executed as long as true.


## Break & Continue

- a break statement can be used to terminate a loop (only the one, it is located in.)
- inside the for-loop, the continue causes control to to immediately move to the increment/ decrement statement.
- inside the while or do-while loop, control immediately moves to the condition.

<div style="page-break-after: always;"></div>

## Switch Statement

- The switch statement provides a way to choose between multiple cases based on the value of a single variable (not an expression!). The variable can be an integer number, character, string or enumeration.

```java
int val = ... ;
switch (val) {
    case 0:
        System.out.println("zero");
        break;
    case 1:
        System.out.println("one");
        break;
    case 2:
        System.out.println("two");
        break;
    default:
        System.out.println("The value is less than zero or greater than two");
}
```

## Methods

- Naming: one word SCHOULD be a verb. Two words verbSomething.

```java
public static int countSeeds (int parrotWeight, int parrotAge) {
    
    return parrotWeight / 5 + parrotAge;
}
```

- public static = modifiers
- int = return type
- countSeeds = method name
- (int parrotWeight; int parrotAge) = list of parameters
- {         } = body
- Methods have different types of calling/ invoking.

``findUserByName("Kate");``
``Math.round(79.565);`` This method is called from outside a class, indication of name of class as prefix.

- There are non-access and access modifiers
- access-modifiers = public, private -- define visibility of a method.
- non-access-modifiers = static (means method belongs to class and can be accessed without creating an object. Without static -> instance method.
- in parentheses definition of type, number and order of the parameters.
- return type: int, double, void (no return type)
- signature = name of method (parameter-type, parameter-type) -> sell(int, int)


## Classes

- A class is declared with the class keyword followed by the class name and the body.

```java
class Nothing {
    // empty body
}
```

- Class body can include: fields (store data), methods (define behaviour) and constructors (create and initialise new objects of the class).
- A field is a variable that stores data. It may have any type, including primitive types (int, float, boolean and so on) and classes (even the same class). A class can have as many fields as needed.

- Object: create an object of the class patient using keyword new:

```java
Patient patient = new Patient();
```

- When creating an object, each field is initialised with the default value of a corresponding type.


## Constructors

- Special methods that initialise new object (instance) of the class.
- Has the same name as the class that contains it.
- Has no return type, not even void.
- If a class has no explicit constructors, the Java compiler automatically provides a default no-argument constructor.
- If we want to introduce new variables to denote the same thing, make the code clearer and less loaded with extra variables, the keyword **this** is used.

```java
class Patient {
    
    String name;
    int age;
    float height;

    public Patient(String name, int age, float height) {
        this.name = name;
        this.age = age;
        this.height = height;
    }
}
```

<div style="page-break-after: always;"></div>

### Math / Random

```java
// Generate a random number
double random = Math.random();
System.out.println(random); // Output: a random double between 0 (inclusive) and 1 (exclusive)

// Round a double to the nearest integer
double pi = 3.14159265358979323846;
int rounded = (int) Math.round(pi);
System.out.println(rounded); // Output: 3

// Raise a number to a power
double base = 2;
double exponent = 3;
double result = Math.pow(base, exponent);
System.out.println(result); // Output: 8.0

// Find the square root of a number
double number = 9;
double squareRoot = Math.sqrt(number);
System.out.println(squareRoot); // Output: 3.0

// Find the absolute value of a number
double negative = -5;
double absolute = Math.abs(negative);
System.out.println(absolute); // Output: 5.0

// Find the maximum or minimum of two numbers
double a = 3;
double b = 5;
double max = Math.max(a, b);
System.out.println(max); // Output: 5.0
double min = Math.min(a, b);
System.out.println(min); // Output: 3.0

// Generate a random integer within a specific range 
int min = 10; 
int max = 20; 
int range = max - min + 1; 
int randomInt = (int) (Math.random() * range) + min; System.out.println(randomInt); // Output: a random integer between 10 (inclusive) and 20 (inclusive)

//Generate a random element from a list
List<Integer> list = new ArrayList<>(Arrays.asList(1,2,3,4,5));
Random rand = new Random();
int randomIndex = rand.nextInt(list.size());
int randomElement = list.get(randomIndex);
System.out.println(randomElement); // Output: a random element from the list


```

## Array List

- Stores only objects
- Wrapper class for primitive types must be used: Integer for int. (Integer is the associated wrapper class for int, to wrap it in an object)
- Variable size
- Slower than Array, because indexing has to be done when removing, adding elements, takes time!
- Array List and Array's can be changed to one another!
- ArrayLists have variable size which dynamically adjusts to the number of elements.
- `ArrayList<String> myFriends = new ArrayList<>();` 
	Declaration: <> is called a diamond  operator. It is not needed anymore in later versions of Java to declare `<String>` a second time.
- `import java.util.ArrayList;` needed

```java
import java.util.ArrayList;

public class ArrayListExample {
    public static void main(String[] args) {
        ArrayList<Integer> numbers = new ArrayList<Integer>();
        
        // add elements to the ArrayList
        numbers.add(1);
        numbers.add(2);
        numbers.add(3);
        
        // retrieve an element at a specific index
        int firstNumber = numbers.get(0);
        System.out.println("The first number is: " + firstNumber);
        
        // remove an element at a specific index
        numbers.remove(1);
        System.out.println("The numbers list after removing the second element: " + numbers);
        
        // check if an element is in the ArrayList
        boolean containsThree = numbers.contains(3);
        System.out.println("The numbers list contains the number 3: " + containsThree);
        
        // get the size of the ArrayList
        int size = numbers.size();
        System.out.println("The size of the numbers list is: " + size);
    }
}
```


## Array's

- Stores objects and primitive data types.
- Array's are collection of elements of the same type.
- Possible number of elements to be stored is established when the array is created and cannot be changed, but stored elements can be changed any time.
- Index from 0 to x.
- Array is a reference type
- Last element is accessed by index equal to array size -1
- Possible to store elements of any type in an array

``int[] array`` declaration form 1
``int array[]`` declaration form 2, less used in practice

- Creating an Array: 
    - declaration: declare variable of array type
    - instantiation: create instance of array object
    - initialisation: initialise array by some values

```java
int n = 5; // n is the lenght of the array.
int[] numbers = new int[n];
```

```java
Object[] objectArray = new Object[] (object1, object2, object3)
```

- ``Object[] objectArray =`` declaration
- ``new Object[]{    }`` instantiation
- ``object1, object2, object3`` initialisation
- Different ways
``int a = 1, b = 2, c = 3;``
``int[] numbers = (a, b, c);``
``int[] numbers = {1, 2, 3, 4, 5};``
- Length of an array:
``int lenght = numbers.lenght; // numbers = name of the array``
- The length is now stored in the variable ``lenght``.
- Accessing elements:
``array[index] = val;`` set the value by the index
``val = array[index];`` get the value by the index
- for ex: ``int val = numbers[3];`` gets the fourth element with index 3.

## TreeSets

```java
// Create a new TreeSet
TreeSet<Integer> treeSet = new TreeSet<>();

// Add an element to the TreeSet
treeSet.add(10);
treeSet.add(5);
treeSet.add(15);

// Get the first (lowest) element in the TreeSet
Integer first = treeSet.first();
System.out.println(first); // Output: 5

// Get the last (highest) element in the TreeSet
Integer last = treeSet.last();
System.out.println(last); // Output: 15

// Get the element just lower than a specified element
Integer lower = treeSet.lower(12);
System.out.println(lower); // Output: 10

// Get the element just higher than a specified element
Integer higher = treeSet.higher(12);
System.out.println(higher); // Output: 15

// Remove an element from the TreeSet
treeSet.remove(10);

// Check if an element is present in the TreeSet
boolean contains = treeSet.contains(5);
System.out.println(contains); // Output: true

// Get the size of the TreeSet
int size = treeSet.size();
System.out.println(size); // Output: 2

// Clear the TreeSet
treeSet.clear();

// Check if the TreeSet is empty
boolean isEmpty = treeSet.isEmpty();
System.out.println(isEmpty); // Output: true


```

## HashSets

```java
// Create a new HashSet
HashSet<Integer> hashSet = new HashSet<>();

// Add an element to the HashSet
hashSet.add(10);
hashSet.add(5);
hashSet.add(15);

// Remove an element from the HashSet
hashSet.remove(10);

// Check if an element is present in the HashSet
boolean contains = hashSet.contains(5);
System.out.println(contains); // Output: true

// Get the size of the HashSet
int size = hashSet.size();
System.out.println(size); // Output: 2

// Clear the HashSet
hashSet.clear();

// Check if the HashSet is empty
boolean isEmpty = hashSet.isEmpty();
System.out.println(isEmpty); // Output: true

// Iterate over the elements in the HashSet using an iterator
Iterator<Integer> iterator = hashSet.iterator();
while (iterator.hasNext()) {
    Integer value = iterator.next();
    System.out.println(value);
}

// Iterate over the elements in the HashSet using a for-each loop
for (Integer value : hashSet) {
    System.out.println(value);
}

// Copy the elements of the HashSet to an array
Integer[] array = hashSet.toArray(new Integer[hashSet.size()]);

// Retain only the elements in the HashSet that are also in a specified collection
HashSet<Integer> otherSet = new HashSet<>();
otherSet.add(10);
otherSet.add(20);
hashSet.retainAll(otherSet);

// Remove all the elements in the HashSet that are also in a specified collection
HashSet<Integer> otherSet = new HashSet<>();
otherSet.add(10);
hashSet.removeAll(otherSet);
```

### Dates, Time, Duration and Period

```java
// Get the current date and time
LocalDateTime now = LocalDateTime.now();
LocalDate today = LocalDate.now();
LocalTime nowTime = LocalTime.now();

// Create a LocalDateTime, LocalDate and LocalTime object with specific values
LocalDateTime specificDateTime = LocalDateTime.of(2022, Month.JULY, 15, 12, 30, 45);
LocalDate specificDate = LocalDate.of(2022, Month.JULY, 15);
LocalTime specificTime = LocalTime.of(12, 30, 45);

// Get the year, month, day, hour, minute, and second from a LocalDateTime, LocalDate and LocalTime object
int year = specificDateTime.getYear();
Month month = specificDateTime.getMonth();
int day = specificDateTime.getDayOfMonth();
int hour = specificDateTime.getHour();
int minute = specificDateTime.getMinute();
int second = specificDateTime.getSecond();

// Compare two LocalDateTime, LocalDate and LocalTime objects
LocalDateTime dateTime1 = LocalDateTime.of(2022, Month.JULY, 15, 12, 30, 45);
LocalDateTime dateTime2 = LocalDateTime.of(2022, Month.JULY, 15, 12, 30, 45);
boolean isEqual = dateTime1.isEqual(dateTime2);

LocalDate date1 = LocalDate.of(2022, Month.JULY, 15);
LocalDate date2 = LocalDate.of(2022, Month.JULY, 15);
boolean isEqual = date1.isEqual(date2);

LocalTime time1 = LocalTime.of(12, 30, 45);
LocalTime time2 = LocalTime.of(12, 30, 45);
boolean isEqual = time1.equals(time2);

// format LocalDateTime, LocalDate, LocalTime to a string
DateTimeFormatter formatter = DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss");
String formattedDateTime = specificDateTime.format(formatter);
System.out.println(formattedDateTime); // Output: 2022-07-15 12:30:45

// parse a string to LocalDateTime, LocalDate, LocalTime
LocalDateTime parsedDateTime = LocalDateTime.parse("2022-07-15 12:30:45", formatter);
LocalDate parsedDate = LocalDate.parse("2022-07-15", formatter);
LocalTime parsedTime = LocalTime.parse("12:30:45", formatter);

```

```java
LocalDateTime specificDateTime = LocalDateTime.of(2022, Month.JULY, 15, 12, 30, 45);
LocalDate specificDate = LocalDate.of(2022, Month.JULY, 15);
LocalTime specificTime = LocalTime.of(12, 30, 45);

// Add or subtract a certain amount of time to a LocalDateTime, LocalDate, and LocalTime object
LocalDateTime addedDateTime = specificDateTime.plusDays(2).plusHours(3).plusMinutes(15);
LocalDate addedDate = specificDate.plusMonths(1).plusYears(2);
LocalTime addedTime = specificTime.plusSeconds(30).plusNanos(500000);

LocalDateTime subtractedDateTime = specificDateTime.minusDays(2).minusHours(3).minusMinutes(15);
LocalDate subtractedDate = specificDate.minusMonths(1).minusYears(2);
LocalTime subtractedTime = specificTime.minusSeconds(30).minusNanos(500000);

// Subtract one LocalDateTime, LocalDate, and LocalTime from another to get a Period or Duration
LocalDateTime dateTime1 = LocalDateTime.of(2022, Month.JULY, 15, 12, 30, 45);
LocalDateTime dateTime2 = LocalDateTime.of(2023, Month.JANUARY, 20, 15, 45, 30);
Period period = Period.between(dateTime1.toLocalDate(), dateTime2.toLocalDate());
Duration duration = Duration.between(dateTime1, dateTime2);
```

```java
// Create a Duration object
Duration duration1 = Duration.ofSeconds(3600); // 1 hour
Duration duration2 = Duration.ofMinutes(60); // 1 hour
Duration duration3 = Duration.ofMillis(3600000); // 1 hour
Duration duration4 = Duration.ofNanos(3600000000000L); // 1 hour

// Create a Period object
Period period1 = Period.ofYears(1);
Period period2 = Period.ofMonths(12);
Period period3 = Period.ofWeeks(52);
Period period4 = Period.ofDays(365);

// Add or subtract a Duration or Period from a LocalDateTime, LocalDate, or LocalTime object
LocalDateTime dateTime = LocalDateTime.of(2022, Month.JULY, 15, 12, 30);
LocalDate date = LocalDate.of(2022, Month.JULY, 15);
LocalTime time = LocalTime.of(12, 30);

LocalDateTime addedDateTime = dateTime.plus(duration1);
LocalDate addedDate = date.plus(period1);
LocalTime addedTime = time.plus(duration2);

LocalDateTime subtractedDateTime = dateTime.minus(duration1);
LocalDate subtractedDate = date.minus(period1);
LocalTime subtractedTime = time.minus(duration2);

// Get the amount of time represented by a Duration or Period object
long seconds = duration1.getSeconds();
int nanos = duration1.getNano();
int years = period1.getYears();
int months = period1.getMonths();
int days = period1.getDays();

// Compare two Durations or Periods
Duration duration5 = Duration.ofHours(2);
Duration duration6 = Duration.ofMinutes(120);
Period period5 = Period.ofMonths(6);
Period period6 = Period.ofDays(180);

duration5.compareTo(duration6); // 0
period5.compareTo(period6); // 0

```

## Inheritance

```java
// Parent class (also known as superclass or base class)
class Vehicle {
    int wheels;
    String color;

    public Vehicle(int wheels, String color) {
        this.wheels = wheels;
        this.color = color;
    }

    public void startEngine() {
        System.out.println("Engine started.");
    }
}

// Child class (also known as subclass or derived class)
class Car extends Vehicle {
    int doors;

    public Car(int wheels, String color, int doors) {
        // Call the constructor of the parent class
        super(wheels, color);
        this.doors = doors;
    }

    public void honkHorn() {
        System.out.println("Beep beep!");
    }
}

// Usage
Car myCar = new Car(4, "red", 4);
myCar.startEngine(); // Output: "Engine started."
myCar.honkHorn(); // Output: "Beep beep!"
```

A class that inherits from another class is called a subclass, and the class that is being inherited from is called the superclass. In Java, a class can inherit from only one superclass (single inheritance).

Java provides a mechanism of inheritance using the keyword `extends`. The subclass can access the public and protected members (fields and methods) of the superclass. This mechanism helps in reusing the code functionality and avoids rewriting the same code in different parts of the program.

```java
class Parent {
    protected int x;

    public Parent() {
        x = 5;
    }

    public void printX() {
        System.out.println("Parent x: " + x);
    }
}

class Child extends Parent {
    private int x;

    public Child() {
        super(); // call the constructor of the parent class
        this.x = 10;
    }

    public void printX() {
        System.out.println("Child x: " + x);
        super.printX(); // call the printX method of the parent class
    }
}
```

In this example, the `Child` class extends the `Parent` class and has a private field `x` with a different value. The `Child` class also overrides the `printX` method from the parent class. When we call `super.printX()` in the child class, it allows us to access the parent class method and print the value of `x` from the parent class, even though it's not accessible from the child class because it's private in the child class.

It's also possible to use the `super` keyword in a constructor to call the constructor of the parent class. In the Child class constructor above we use `super();` to call the constructor of the parent class, so that the `x` field is initialized to the value specified in the parent class.


## MVC - Model, View, Controller
*The Model View Controller separates the calculations and data from the interface*

* **View**: The Interface.  The View handles, what is beeing viewed. Gets data from model through methods. View does not know about controller and model. It is possible, that the view knows about the model to display data from the beginning.
* **Model**: Data and Methods used to work with the Interface. The model contains the data, performs the methods/calculations and provides access to the data. Model does not know about view and controller.
* **Controller**: Coordinates interactions between the View and the Model. Controller knows about the view and model. Controller just handles the interactions between the view and the model.
* **The MVC Class ** is creating the objects and contains the main method.

**MVC** (**Model-View-Controller**) is an architectural pattern separating an application into three logical components:

-   **Model** is responsible for all data and its related logic;
-   **View** is responsible for presenting data to users or handling user interaction;
-   **Controller** informs the Model of the need for changes.

![[Model-View-Controller_Relation.png|100]]
- There are different approaches to the way which component acesses what. At FHNW, we learned the follwoing:
 
![[Model-View-Controller_Relation2.png|300]]

<div style="page-break-after: always;"></div>

# JavaFX

- To run a JavaFX Application, JavaFX lib must be added to project structure, libraries for every Main class.
- Also to run the Program, JavaFX lib must be added to the VM options or configuration arguments.
- **--module-path /Users/myname/JavaFX/javafx-sdk-17.0.0.1/lib --add-modules javafx.controls,javafx.fxml,javafx.media**
- Error: JavaFX runtime components are missing and are required to run this application.

## Terminology and Basics

- Stage = Main Window
- Scene = all content of main Window
- Group = serves as root node of a scene
- every JavaFX Program must:
- "extends Application"
- Stage primaryStage;
- Scene scene1 = new Scene(content, width, height);
- primaryStage.setTitle("a JavaFX Program");
- primaryStage.setScene(scene1);
- primaryStage.show();

<div style="page-break-after: always;"></div>

## Lifecycle of a JavaFX Program

```java
public class Flags03 extends Application {
    public static void main(String[] args) {
        launch();
    }
/*
JavaFX program must have a public class which extends application.
also it must have a main method, which calls launch()
launch(args) would take in command line parameters if ther would be any.
*/
    @Override
    public void init() {

    }
/*
init method does not have to be invoked. There is a standard init method that will be invoked
if there is no init method, which does nothing. This method is for constructor code.
*/
    @Override
    public void start(Stage primaryStage) {

    }
/*
The start Method does have to be called. There is no default method.
This is where all the important code for GUI elments will be written.
Start a Stage (Main Window) and import javafx.stage.Stage
*/
    @Override
    public void stop() {

    }
}

// The stop method will execute code, when the program is stopped.
```

# Basic Shapes

- JavaFX shapes are represented by classes in the javafx.scene.shape package
- A line segment is defined by the **Line** class, whose constructor accepts the coordinates of the two endpoints:
	Line(startX, startY, endX, endY)
	``Line myLine = new Line(10, 20, 300, 80);``
- A rectangle is specified by its upper left corner and its width and height:
	Rectangle(x, y, width, height)
	``Rectangle r = new Rectangle(30, 50, 200, 70);``
- A circle is specified by its center point and radius: 
	Circle(centerX, centerY, radius)
	``Circle c = new Circle(100, 150, 40);``
- An ellipse is specified by its center point and its radius along the x and y axis: 
	Ellipse(centerX, centerY, radiusX, radiusY)
	``Ellipse e = new Ellipse(100, 50, 80, 30);``
- Shapes are drawn in the order in which they are added to the group. 


# Additional Links

Color-codes: https://www.rapidtables.com/web/color/RGB_Color.html



















