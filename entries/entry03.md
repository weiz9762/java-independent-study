
## Entry 3: Plans Always Fall Behind Changes: Some Superficial Knowledge of Java Class
---
### Week Three Started!!!

After spending a lot of time exploring Java syntax, I was finally able to take a small peek on how to collect user input. All I had to learn previously were how to manipulate data in the backend, and this week I learned a little bit about how to take in user's input and manipulate them with the methods created.

---

### Input

Collecting user input in Java is _**complicated**_, let's take a look of a code snippet.

``` Java
Scanner scanner = new Scanner(System.in);

        System.out.println("Enter your year of birth: "); // print out the question in console

        boolean hasNextInt = scanner.hasNextInt(); // check if the input is number

        if (hasNextInt) { // if the input is number
            int yearOfBirth = scanner.nextInt(); set yearOfBirth to user input and convert it into integer datatype
            scanner.nextLine(); // handle the "enter" press
            int age = 2019 - yearOfBirth; // calculate the age

            System.out.println("Enter your name: ");
            String name = scanner.nextLine();

            if(age >= 0 && age <= 100) {
                System.out.println("You name is " + name + ", and you are " + age + " years old");
            } else {
                System.out.println("Invalid year of birth");
            }
        } else {
            System.out.println("Invalid input");
        }
        
        scanner.close();

```

In the previous week, all the syntax in Java, to some extent, look similar to Ruby syntax. But Scanner is completely different, it does not look like anything in Java. Ok! Let's explain what the code above does.
+ **S**canner: build in Java class that use to read user keyword
+ **s**canner: a variable defined that calls method `nextLine` to read the line of input from the console
  - `nextLine();` is a method that  telling the program to take in the user input after "enter" key was pressed
  - `nextInt();` in default, the input will be treat as a string, and this method auto convert input (string) to an integer
  - `.hasNextInt();` is a method to check if user input is an integer (or specifically a string that can be converted into an integer
+ `System.in` the information is typed into the console and returns back to the program
+ `System.out` the information being displayed to console
+ `scanner.close();` use to close the scanner in which saves the memory
+ The if and else statement is basically used to calculate user's age according to user input

However, despite the fact that code is running properly, I was wondering if the variable "scanner" has to be "scanner". Since there are too many scanners, it kind of confused me what scanner to use. Therefore, I wonder what if I replace `scanner` with `question` since the information display in the console is technically a question for the user to answer, so I change code into something like this: 

``` java

Scanner question = new Scanner(System.in);

        System.out.println("Enter your year of birth: ");

        boolean hasNextInt = question.hasNextInt();

        if (hasNextInt) {
            int yearOfBirth = question.nextInt();
            question.nextLine();
            int age = 2019 - yearOfBirth;

            System.out.println("Enter your name: ");
            String name = question.nextLine();

            if(age >= 0 && age <= 100) {
                System.out.println("You name is " + name + ", and you are " + age + " years old");
            } else {
                System.out.println("Invalid year of birth");
            }
        } else {
            System.out.println("Invalid input");
        }

        question.close();
```

As it turns out, it works, and the code is now a bit easy for me to understand and recreate in the future. The capital Scanner, however, cannot be replaced because it's a build it class in Java with its own function. Since we talked about class, what exactly is the class?


---
### Parsing

Parsing is used to turn a string into other data types

``` java
Integer.parseInt("1232324");

==> 1232324

// Integer is the wrapper class of int
// .parseInt(); is the method that change string into int
// if convert failed, will return error
```

The parsing method exist in other primitive datatypes also but with different method names. Folling are some examples:
+ `Long.parseLong();`
+ `Boolean.parseBoolean();`

---


### What is Class?
We talked about that Java is an object-oriented language, so what does it suppose to mean?

- In Java, an object is just like an object in real life, it's something has its state (variable) and behavior (method)
- Class, on the other hand, is the template for creating an object

In short, the class is a _bigger_ method that teaches the computer how to make an object with a similar identity.

###### _[And See more here :see_no_evil:](https://docs.oracle.com/javase/8/docs/api/java/lang/Class.html)_

Here is an example of a Car class:

```java
public class Car { // creating a Car class

    private int doors; // each car will have these properties 
    private int wheels;
    private String model;
    private String engine;
    private String color;

    public void setModel(String model) { // setter (assign property to an value, usually a user input
        String validModel = model.toLowerCase();
        if (validModel.equals("porsche") || validModel.equals(("holden"))) {
            this.model = model;
        } else {
            this.model = "Unknown";
        }
    }

    public String getModel() { // getter (getting the information of the property)
        return this.model;
    }
}
```

```java

Car porsche = new Car();// creating a new car and assign it to variable porsche
porsche.setModel("porsche"); // assign prosche's model to "porsche" using .setModel method created in the class
System.out.println(porsche.getModel()); // return porsche's model using .getModel method created in the class
}

```

The class in Java is similar to the class in Ruby, except the syntax difference. I was planned to finish learning all the "class" lesson this week, but my goal was not fully met due to many other events happened at the same time. I was able to learn about the constructor of the Java class, but I did not fully understand it yet, so I will put it into my next entry when I become more familiar with it. I was not quite happy about my progress this week because I was not able to plan everything ahead of the time. Therefore, my plans are following behind the change in which I need readjust my plan for different unexpected moments. However, I'm definitely the only one facing this issue, and I'm happy that I see the problem now, so I can be better prepared in the future.

--- 






### Takeaway
1. Just like my entry title says, plans always fall behind changes. There are so many things that are completely unexpected to you, and they are just conflicting with your plan. However, all you need to do is to accept the change and readjust your plan. Stay patient, stay positive, and stay active.
2. Always try stuff out even if things are completely unfamiliar to you. The way others understand something might not be the best way for you. Explore the way that is best for you instead of just blindly follow other's instructions.

---
### Notes:
+ equals(); to compare if two value are the same
+ public: make a class with unrestricted access
+ Integer.MAX_VALUE: a constant in integer class that is equivalent to the max value for integer datatype 
+ Integer.MIN_VALUE: a constant in integer class that is equivalent to the min value for integer datatype 
+ Boolean flag: a boolean can be true or false










