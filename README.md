# Java-Docu
My own personal collection of Java Code. Good to knows and more.

# General

## Print
```java
System.out.println("Hello World");
```

## Input
```java
import java.util.Scanner;
Scanner sc = new Scanner(System.in);
String input = sc.nextline();
sc.close();
```

## Declaration of Variables
```java
// <type> <variable>
int count;
```

## Declaration & Initialization of Variables
```java
int count = 5;
```

## Operators
```java
int n = 17;
int o = n++; // o = 17; n = 18 first initialization then n+1
int p = ++n; // p = 19; n = 19 first n+1 then initialization
```

## primitive Datatypes
```java
// Integers
byte // 8 Bit -128 to 127
short // 16 Bit -32.768 to 32.767
int // 32 Bit -2.147.483.648 to 2.147.483.647
long // 64 Bit

// Decimals
float f = 11.3f; // 32 Bit
double d = 103.0489d; // 64 Bit

// Booleans
boolean bt = true;
boolean bf = false;

// Characters
char c = 'c'; // only for single Characters
```

## Comparisons

### **Equality**
```java
// between primitive Datatypes
int i = 6;
int j = 7;
i == j // return false
// if used on objects tests if it is the exact same object (pointing to same storage cell)

// between objects for value comparison (eg. Strings)
String s1 = "test";
String s2 = "test";
s1.equals(s2); // return true
// Tip: If one of the two could be null, put it last, thus avoiding a null pointer exception
```

### **Greater, Smaller, Not**
```java
// greater than or equal
>=

// less than or equal
<=

// not
!=
```

### **Logical Comparisons**
```java
int i = 5;
boolean b = true;

// AND - requires 2 true's
(i > 4) && (b) // return true

// OR - requires at least 1 true
(i > 6) || (b) // return true
```

## Conditions
```java
int i = 5;
if (i < 5) {
    ;
} else if (i > 5) {
    ;
} else {
    ;
}

// () can also contain multiple conditions => ((i > 5) && (b == 6))
```

## Loops
```java
// for-loops when the number of iterations is clear
for (int i = 0; i < 10; i++) {
    System.out.println(i);
}

// while-loops to test conditions, when the number of iterations is unclear
int i = 0;
while (i < 10) {
    System.out.println(i);
    i++;
}

// do-while-loops for cases where you need to execute a loop at least once no matter what
int i = 0;
do {
    System.out.println(i);
} while (i < 10);
// returns 0, then breaks
```

### **Break**
```java
int i = 0;
while (i < 7) {
    System.out.println(i);
    i++;
    if (i == 3) {
        break;
    }
}
// return 0, 1, 2
// breaks out of most inner loop, also applicable to switch-case
```

# Classes
```java
public class Person {

    public String prename;
    public String surname;
    private int calls = 0;

    public String getName() {
        String name = prename + " " + surname;
        raiseCalls()
        return name;
    }

    private void raiseCalls() {
        calls++;
    }
}
```

## Constructor
```java
// address Object attributes with "this.", to differentiate between passed parameters
public class Person {

    public String prename; // Declaration
    public String surname;
    private int calls = 0; // Initialization to standard value

    // empty Constructor, overrides Default Construcotr
    public Person () {
        this.prename = "John";
        this.surname = "Smith";
        this.calls = 0;
    }

    // Constructor with Parameters
    public Person (String prename, String surname, int calls) {
        this.prename = prename;
        this.surname = surname;
        this.calls = calls;
    }
}
```

## Creating an Object
```java
import package_name.Person;
Person p1 = new Person(); // empty Constructor is called
Person p2 = new Person("Frank", "Schmitt", 8) // Constructor with the corresponding Attribute count (+ Datatype matches) is called
```

## Using a Method
```java
import package_name.Person;
Person p = new Person("Frank", "Schmitt", 8);
Sytsem.out.println(p.getName());
```

## Methods
```java
public class Person {

    public String prename;
    public String surname;
    private int calls = 0;

    public Person (String prename, String surname, int calls) {
        this.prename = prename;
        this.surname = surname;
        this.calls = calls;
    }

    // Method with no return value
    public void raiseCalls () {
        this.calls++;
    }
}
```

### **Getter/Setter**
```java
// central way of assigning / changing attributes of an Object
public class Person {

    public String prename;
    public String surname;
    private int calls = 0;

    public Person (String prename, String surname, int calls) {
        this.prename = prename;
        this.surname = surname;
        this.calls = calls;
    }

    // obtain current object's surname
    public String getSurname () {
        return this.surname;
    }

    // set current object's surname
    public void setSurname (String surname) {
        this.surname = surname;
    }
}
```

### **to-String**
```java
public class Person {

    public String prename;
    public String surname;
    private int calls = 0;

    public Person (String prename, String surname, int calls) {
        this.prename = prename;
        this.surname = surname;
        this.calls = calls;
    }

    @Override // Tag to overwrite the Default to String Method
    public String toString() {
        return "Person{" +
                "prename='" + this.prename + '\'' +
                ", surname='" + this.surname + '\'' +
                ", calls=" + this.calls +
                '}';
    }

}
```

## Static

## **Attributes**
```java
// Static Attributes count for the Class as a whole, so they are only accessible once instead of per Object
public class Person {

    // static indicates a Class Attribute
    public static int persons_created = 0;
    public String prename;
    public String surname;
    private int calls = 0;

    public Person (String prename, String surname, int calls) {
        this.prename = prename;
        this.surname = surname;
        this.calls = calls;
        Person.persons_created++; 
    }

}
// to access Class Attributes: classname.static_attribute_name
```

## **Methods**
```java
```java
// Static Methods are available once for the Class, not every Object
public class Person {

    public static int persons_created = 0;
    public String prename;
    public String surname;
    private int calls = 0;

    public Person (String prename, String surname, int calls) {
        this.prename = prename;
        this.surname = surname;
        this.calls = calls;
        Person.persons_created++;
    }

    // static indicates a Class Method
    public static int getPersonsCreated () {
        return Person.persons_created;
    }

}
// to access Class Methods: classname.static_method_name(parameters)
```


# Modifier
```java
public
friendly
protected
private
```


### **Tuple Return**
```java

```

# Modules

## Module 1
```java

```

### **Module 1 Functionality 1**
```java

```