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

### Equality
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

### Greater, Smaller, Not 
```java
// greater than or equal
>=

// less than or equal
<=

// not
!=
```

### Logical Comparisons
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

### Break
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