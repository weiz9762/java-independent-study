## Entry 2: That Looks Familiar: Method, Conditional, and Loop
---
### Let's take a deep dive :ocean:!

After learning the primitive datatypes and operator, I dived deeper into the world of Java. There were many coding
challenges incorporated into the course, and I became more familiar with what I learned previously in which built a 
strong foundation of more complex Java lesson. This week, I focused on Java's control flow statement in which I found a lot of similarity with Ruby. However, because of these similarities, I often forgot that I'm programming in Java, 
 thus, writing much code that returned an error during the process.

---


### What is the control flow statement?
Usually, the code is executed on the first come first serve bases (from top to bottom in which they appear). Control
 flow statements, as it sounds, control the flow of execution. In Java, there are three types of control flow 
 statement:
+ The conditional statements (if-else, if-then-else, switch)
+ The looping statements (for, while, do-while)
+ The branching statements (break, continue, return)

###### _[And See more here :see_no_evil:](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/flow.html)_



--- 

### The Conditional Statement

#### if statment

The if statement is used to execute a block of code if the condition is met. The structure of if statement is the following:
``` java
If (condition) {
    code // if the first condition is true, run this block 
} else if (condition) {
    code // if the previous condition is false, run this block
} else {
    code // if none of the condition is true, run this block
}
```

---

#### switch

The switch statement is the alternative of the if statement, and it's great for the evaluation of the variable. Here is a
 example:
 
```java
switch(variableName) { // evaluate the variable  
    case value1: // if variable is equal to value 1
        code; // run this code
        break; // exit the switch statement
    case value2:
        code;
        break;
    default: // if variable is not equal to value1 or value2
        code; // run this code instead
        break;
}
```

---
### The Looping Statement
loop: use to execute code multiple times until a certain condition is satisfied 


#### for loop
Use for repeat a block of code when you know how many time you want the loop to run. For instance, the code below will run 9 times.  


```java
for(int i = 0; i < 10; i++) { 
    code
    // int i = 0; set up the initial condition by creating a variable
    // int i < 10; until i not longer smaller than 10, it will keep looping
    // i++, the i will increase by one each time the code loop
}
```

#### while loop
On the other hand, when you don't know how many time you want to loop, you can use a while loop.

```java
int count = 0; // set up a variable count
while (count != 5) { // while count is not equal to 5, the code below will run
      System.out.println(count);
      count ++; // everytime it loop, the count will increase by 1 until count is equal to 5
}
```

#### do-while loop
The do-while loop is similar to while loop except the code will run at least once

```java
int count = 6;
do { // run the code below first
    System.out.println(count);
    count++;
} while (count < 6); // code is not smaller than 6, so the loop exit
```

---
### branching statement

#### return & break & continue
+ Return: send back the information, when return processed, the code will not going further
+ Break: terminates the enclosing switch statement and control continues after the block
+ Continue: allow the loop to continue, but if the statement is true the code afterward will not execute (continue to 
next iteration) and bypass all other code in the block


---

### Something Different From Ruby: Method Overloading 
Method overloading is the method using the same method name with different parameter (_*change the return data type will not 
work_)

```java
    public static int calculateScore(String playerName, int score) {
        System.out.println("Player " + playerName + " scored " + score + " points");
        return score * 1000;
    }

    public static int calculateScore(int score) {
        System.out.println("Unnamed player scored " + score + " points");
        return score * 1000;
    }

    public static int calculateScore() {
        System.out.println("no player name, no player score");
        return 0;
    }
```

Three methods above share the same method number, but with different parameters. According to the parameters given, the 
Java will determine which method to be executed.

---
### Story Time!
When I was working on my coding challenges, it asked me to write a method that takes in a number and add every significant of the number together. (i.e. 213 will prints out 6 [2+1+3]). I came up with something like this:

```java 
private static int sumDigits(int number) {
    if (number < 10) {
        return -1;
    } else {
        int single = number % 10;
        int tenth = (number % 10) % 10; // error occurs here
        int hundred = number / 100;
  
        return (single + tenth + hundred);
    }
}
```
However, it was not working as I expected, and I can't really figure out why. As a result, I commented out the code
 above and redid the coding challenge in which I found `int tenth` should equal to `(number / 10) % 10`. Then I 
 checked the solution given in the course:

```java
private static int sumDigits(int number) {
        if (number < 10) {
            return -1;
        }

        int sum = 0;

        while (number > 0) {
            int digit = number % 10;
            sum += digit;
            number /= 10;
        }

        return sum;
      
    }
```
WOW, it's totally different from mine. The solution given used the loop statement in which will work with any number given. My solution, on the other hand, only worked with the three-digit number. Therefore, I adopt the given solution but using the for loop which worked quite nicely.

---
### Takeaway
There are always different ways to solve the problem. "All road lead to Rome". Maybe your solution is not the most effective solution, but it's the _right_ solution. However, it's always good to see other approaches that are different from yours so you can understand how to make your solution _better_. In addition, It's **okay** to start over, when stuff is not working, leave it for now, try to redo what you did, and come back to check why it was not working the first time. 

### Notes:
+ Constant: a variable that has assigned value that is immutable
    + Should be upper case and use _ to separate words
    + Final: keyword to declare constant 
+ Static: can be changed, the variable will only be accessible by static 
+ .toLowerCase(): Method of string class, change characters into lower case
+ Psvm (IntelliJ shortcut): main method (standard entry point for java to run the code)
+ Math.round(), round double or float into an integer











