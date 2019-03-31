## Entry 01 - Intro: Entering the World of Java
---
### So, you ask me **_why_** Java?

Even before the senior year begins, I spent a lot of time thinking about what to do for my independent study. I'm fairly new to the field of computer science, and there is a countless amount of things that intrigue me. The first thing that came to my mind though, is Java and JavaScript. I have no idea what they are and how are they related, (_apparently, they are totally unrelated besides having a very similar name_) but I just to learn about them. I eventually set down on Java just because I'm totally unfamiliar with it, and I want to see how much I can learn in a completely unknown area.

---
### But what is Java anyway?

According to [Oracle](https://www.java.com/en/download/faq/whatis_java.xml), the current owner of Java, "Java is a programming language and computing platform first released by Sun Microsystems in 1995. From laptops to datacenters, game consoles to scientific supercomputers, cell phones to the Internet, **Java is everywhere!**" In short, you can basically create anything you want with Java, (Hmm, maybe not so much on the front-end, see Java-Script for more :relieved:) but overall, it's a super powerful language!

+ It is also known as the simplified (in term of syntax) version of C++. 
+ It is an object-oriented language that utilizes class and method
+ It runs on almost all the operating system (i.e. Windows,  Mac OS, and Linux)

<br> 

![alt text](https://d1jnx9ba8s6j9r.cloudfront.net/blog/content/ver.1553858763/uploads/2018/01/2-2.png "What is Java Used For")

---

### Project Idea

Mr. Mueller told us to think of something we want to do before we chose our topic. Okay, let's be honest, I didn't know what to do at all! When he was talking to Xiurong, Jennifer, and Travis in the class about their project idea, all I hope is that he is not coming for me afterward! Anyway, I spent some time thinking about what I want to do and if it can be achieved by Java. I know for the fact that I want to do a game, either original or remake. Some ideas that I had were
+ Some basic Java game (Tetris, Pacman)
+ Dota 2 Autochess (Since they are so popular now compared to the "real" Dota 2 TGC game a.k.a Artifact)
+ Pokemon (Sherzod claimed that he never played it before, maybe just remake one so he can have some childhood experiences)
+ Telefang (A game that is similar to Pokemon, but it never become popular, but that's my favorite game in my childhood)

I know for the fact that they can all be achieved by Java, it's a matter of time. While I continue to explore Java, I will think about how to make an MVP, and also other possible ideas.

--- 
### Learning and processing

I started with just googling lesson about Java, watched some YouTube video. But I realized that they are not the best option for me because 1) some of the lessons is outdated because Java updated quite frequently 2) reading bunch of code documentation is just not the best way for me to learn something. Therefore, I came across Udemy, and use a Java course taught by Tim Buchalka. I used IntelliJ to do all my Java coding as suggested by Tim. The first week is all about learning the basic, and a lot of the syntax looks very familiar, and below are the notes regarding syntax I organized.

While I was doing a code-along exercise, I met some difficulties. Below was the code I had that return error.

``` java 

public class Main {

    public static void main(String[] args) {
        
    }

    public static int calculateScore(boolean gameOver, int score, int levelCompleted, int bonus) {

        if (gameOver) {
            int finalScore = score + (levelCompleted * bonus);
            finalScore += 2000;
            return finalScore;
        } else {
            return -1;
        }
    }
    
    int highScore = calculateScore(true, 800, 5, 100);
    System.out.println("Your highest score is " + highScore);

    highScore = calculateScore(true, 10000, 8, 200);
    System.out.println("Your highest score is " + highScore);
}
```

According to the error message, `highScore` is an unknown class, and method `calculateScore` is an invalid method declaration
Need call method inside. I didn't quite understand what it means because I did declare the variable and method. However, I realized that my variable and method is not inside any kind of code block since, in Ruby, you can call it wherever you want. Therefore, I move around my code and realized that variable should be called inside 
```java
public static void main(String[] args) {call method here}
```
So I googled what exactly is this, the information I found was quite confusing, but I understand that "this is the name of java main method. It’s fixed and when we start a java program, it looks for the main method."

--- 
### Takeaway
1. Start things early! Because I was aware that we will have an independent study this year, I planned ahead of what I want to study first, so I can just jump right into it when the unit started.
2. It's good to have an idea in mind before you start anything, but if you really can't think about what you want to do, just start something. You can always explore before you fully committed to it.
3. A curriculum designed by professional is the best way for me to learn. It might not be the best approach for others, but that's the best for me. So, just do whatever you think is the best instead of others telling you what is the best

---
### Other Java syntax

#### 8 (Primitive datatypes) + 1 (String class)

|Datatype|Description|Syntax|What is This?|
|:---|:----:|:----:|:----:|
|1. integer|Primitive datatype, default non-decimal number type, a width of 32. Has a min. and max of ± 2.147 million |`int myIntNumber = 8;`|Assigning variable myIntNumber to 8|
|2. byte|Primitive datatype, non-decimal number, a width of 8. Has a min. of -128 to a max. of 127|`int mybyteNumber = 120;`|Assigning variable myByteNumber to 120|
|3. short|Primitive datatype, non-decimal number, a width of 16. Has a min. of -32768 to a max. of 32767|`int myShortNumber = 32700;`|Assigning variable myShortNumber to 32700|
|4. long|Primitive datatype, non-decimal number, a width of 64. Has a min. of -2^31 to a max. of 2^63|`int myLongNumber = 2_000_000l;`|Assigning variable myLongNumber to 2,000,000 (l indicates it's a long datatype) |
|5. float|Primitive datatype, decimal number, a width of 32. Single precision (7 places after demical point)|`float myFloatNumber = 2.0f;`|Assigning variable myFloatNumber to 2.0 (f indicates it's a float datatype) |
|6. double|Primitive datatype, default decimal number type, a width of 64. Double precision (16 places demical point)|`double myDoubleNumber = 3.14159d;`|Assigning variable myDoubleNumber to 3.14159 (d indicates it's a double datatype) |
|7. char|Primitive datatype, single character only, width of 16. |`char registeredSymbol = '\u00AE';`|Assigning variable registeredSymbol to registered symbol |
|8. boolean|Primitive datatype, true or false |`boolean gameOver = true;`|Assigning variable gameOver to true |
|9*. String|**NOT** a primitive datatype, string class |`String myString = "Hello World!;`|Assigning variable gameOver to "Hello, World!" |

--- 
#### Operators
|Operator|Description|
|:---:|:----:|
|=|equal to, used for assignment| 
|*|multiply by| 
|/|divided by| 
|%|Find the remainder| 
|+|add| 
|++|plus 1|
|+=|add and become the sum|
|-|subtract| 
|--|minus 1|
|-=|subtract and become the difference|
|==| equal to, used for evaluation| 
|!=| not equal to, used for evaluation| 
|&&| both condition is true, used for evaluation| 
|| equal to, used for evaluation| 
|>| grater than, used for evaluation| 
|<| smaller than, used for evaluation| 
|>=| grater than or equal to, used for evaluation| 
|<=| smaller than or equal to, used for evaluation| 

---
#### Print
```java 
System.out.println("Hell, World!"); // java command to print something out
```

```java
String myString = "Hello"
System.out.println(myString + " World!");
// return "Hello World!"
```
---
#### Casting
By default, the expression will convert to integer, and casting the the solution for that
```java
short myNewShortValue = (short) (myShortValue / 2); // change the result from integer into a short
```
---
#### `=` v.s. `==`

Since `=` is assignment, it will change the value of the variable
```java 
int newValue = 50;
if (newValue = 50) // return the new value (but if statement require a condition (boolean)
    System.out.println("This is not good");
```
    
```java 
boolean isCar = false;
if(isCar = true) // change the value of var into true, so it will return the below
    System.out.println("This is not supposed to happen");
```
---
#### Ternary 
```java
boolean wasCar = isCar ? true : false
// Evaluate is car, if it’s true, return true (first option), else return false (second option) and the return value will assign to wasCar
```
---
#### If statement

```java
If (condition) {
    do something
} else if (condition) {
    do something else
} else {
    do this instead
} // determine which code block to run
```

Executed by order, if the previous condition was met, the else it will not run

The variable created inside the code block will not be accessed outside the code block, but code block can access the previously definite variable
(*Scope)

---
#### Method

+ Use `public static void` keywords to signal to declare a method 
    + Void = don’t send any value back (do not return)
    + Void can be replaced with different keywords according to what type of data want to be return

+ Parameter will be automatically created as appropriate datatype variable
    + Different from ruby, you don’t need state var = value inside the method because the variable is being created 

+ Calling method: `methodName(argument)`

+ Return = send back the information (value)
    + When return processed, it will not go further
+ You can assign variable to a method


Notes:
+ Src = source
+ Java is case sensitive, cap for Java class
+ Variable = space in memory camelcase using CamelCase (lowUpUp)
+ literal = pure number  
    - When typing literal, you can use underscore (1,000 -> 1_000) to make the number more readable (Java 8+)
+ Unicode-table.com (code for the special character)
+ Comment using //
+ Code block using `{}` to make code clear and making the code be one part in if statement
+ Operator precedence
+ sout = shortcut in IntelliJ for System.out.println
+ Command + Option + L: beautify the code in IntelliJ
+ Java has 53 reserved keyword (predefined meaning)
    - Variable name cannot be reserved keyword
+ expression = Variable + value + operator
    - Datetype and semicolon are not part of a statement
+ Statement = datatype + expression + ;)                      - Java does allow multiple statements in one line (but not recommended)
+ whitespace
    - One space and 10 space treat as the same
    - Java delete the extra spaces internally
+ When adding a string to a number  it converts the number into a string













