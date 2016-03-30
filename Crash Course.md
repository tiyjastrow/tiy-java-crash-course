# Welcome To the Java Crash Course at The Iron Yard!

> a journey of a thousand miles begins with a single step
> - the Tao Te Ching 

**Question:** How do you get to San Francisco from here? 

Perhaps you plug San Fran into your GPS, get on the road, and do what the GPS tells you to?

<!-- note: there is no GPS for programing. And you don't learn anything with GPS. -->

**Question:** What if you don't have a GPS?

Maybe we could use a map? Pick out a route, get on the road, and watch the signs.

<!-- note: You drive, but you use the map as guidance. A route can be suggested by the map. This is the iron yard 12 week classes. -->

**Question:** What if you don't have a map? 

Hopefully you can find someone who will point you west. You can ask for directions as go along.

<!-- note: this crash course is you being pointed west. good-luck! -->

## What you will learn

I intend to give you enough information in this crash course that you can, at least, head westward.

To write a program is to "speak" in a language a computer can understand. We don't actually "speak" to a computer, but we can write  messages that it can understand. These words aren't in a natural language, though. Instead, they're in a "programming language". 

This class is about the programming language called Java. Java is just one of _hundreds_ of programming languages, but it has the distinction of being the most popular.

To a fresh eye, programming languages often look like gibberish. For example:

```java
int total = scores.stream().mapToInt(Scoreable::getScore).sum();
return total / scores.size();
```

This could be translated into english as something like, "Give me the average of a set of scores." This example is intentionally obtuse, but only to illustrate a point: Java isn't english. 

In this class we'll cover just enough that you can see what direction to head in as you learn Java. This is just the first step in your journey.

## A different way of thinking

Computers are fast, literal, and dumb.

Humans are slow and ambiguous, but smart.

You can tell a human to make you some toast and be fairly certain you'll get something that looks like this:

![toast-on-a-plate.jpg](https://tiy-learn-content.s3.amazonaws.com/49e91d04-toast-on-a-plate.jpg)

But you can't just ask a computer for, well, anything. You need to be painfully explicit about Every. Single. Step. 

![mutant toaster, no toast.jpg](https://tiy-learn-content.s3.amazonaws.com/3d380f26-mutant%20toaster%2C%20no%20toast.jpg)

This is what happens when you ambiguously ask a computer for toast. 

<!-- todo: toaster exercise? IE, have the class tell me how to make toast and screw it up however I can? -->

## How to get the most out of this course

There are a lot of different ways to learn to program, but hopefully you're here because you want a hands-on, challenging, and effective method to learn the basics. 

Here are a few *strongly encouraged* practices that you can use to get the most out of this course.

1. **Answer the questions out loud:** when a lesson asks a question, pause for a moment and actually answer the question. For best results, say it aloud! There is evidence that answering questions, even wrongly, primes your brain to remember and retain information[1].

2. **Do all of the exercises:** Make sure that you actually take the time to do the exercises. Humans aren't very good at just absorbing abstract concepts through reading; they need to visualize, feel, and get practical. You can't learn to program just by reading.

3. **Play with the code:** There will be quite a few examples of Java code in this course. There is evidence that positive emotion increases comprehension and retention, so make changes. Change the examples to something that makes you laugh. See what happens when you add, remove, or change things. Try to engage with the code in a way that is fun, whatever that means for you.

<!-- todo: tell them to ask questions too-->

## Getting started

Programmers use a tool to write code called an Integrated Development Environment. IDEs provide a plethora of tools to make programming easier. I use one called [IntelliJ IDEA](https://www.jetbrains.com/idea/), which I highly recommend. There are many others of varying quality. Another one that is well respected is [Eclipse](http://www.eclipse.org/). 

For this class you will be use a super-basic editor called [compilejava.net](https://www.compilejava.net/). This isn't an IDE, but it is a tool that we can use to experiment with basic Java code.

# What is Java anyhow?

We should probably delve into what exactly Java is. However, this isn't a simple question and could quite quickly lead us down the proverbial rabbit hole. Instead, I'd like to hit on some major points, but leave the rest for you to learn as you move forward.

## Java is a programming language

In English we know that we start sentences with capitol letters and end them with periods, question marks, or exclamation points. We know the basic sentence structure of "subject verb noun". Sentences can be collected together to communicate complex messages. This is the _syntax_ of English. All human languages have their own syntax.

All programming languages also have their own syntax. Java code is written in Java's syntax. Unlike spoken languages, a programming language's rules are _very_ strict. In English, a missing comma isn't the end of the world. You can usually figure out what the writer is trying to say. In Java, a missing semicolon results in a program that won't run at all. Computers don't have intuition.

The programming language Java is the syntax you use to tell the computer what to do.

```java
public class HelloWorld {

    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }

}
```

For now, don't worry about what this code does, just type it into compilejava.net as it is and hit the "Compile & Execute" button.

## The Java compiler

Computers only speak one language: Binary. Ones and zeros. That's it. A CPU receives instructions in binary and it does exactly what the instructions tell it to do. Unfortunately, humans don't speak binary.

Back in the dark ages of programming, programmers created mnemonics, known as _assembly code_, to help learn this binary language. A programmer would write assembly code and later _manually_ translate it to binary using a lookup table.

![Example assembly and binary instructions](https://tiy-learn-content.s3.amazonaws.com/aeef70ab-example%20assembly%20and%20binary%20instructions.png)

No mere mortal wants manually translate assembly code to binary. Good programmers are often lazy, and so eventually programs were created to automatically translate assembly code into binary instructions. These were the first _compilers_.

A compiler takes source code written in a programming language and translates it into binary instructions a CPU can understand.

Over time, compilers mature and add features that take us away from the world of assembly to the world of modern programming languages.

The Java compiler is, well, a compiler. (Surprise!) It takes code you write in the Java language and translates that into something your computer can understand.

Java files are (usually) written in files that have a `.java` extension. The compiled files have a `.class` extension.

<!-- demo: compile the hello world example above using javac. show that you can't just ./helloworld.class to run it.  -->

## The Java Runtime Environment

Java is not compiled for a specific computer. We can't just execute it like any other program. Instead, we need a _Java Runtime Environment_. This is the "Java" that your computer is constantly bugging you to update.

The JRE is actually a virtual computer. It simulates the CPU and hardware of a real computer. The JRE takes the compiled Java code and executes.

The JRE effectively hides from the programmer everything that makes a particular computer unique. Java programers don't need to know how to read files on Windows, Mac, Unix, and your set-top cable box. The JRE already does.

This process of hiding implementation details is called _abstraction_. 

## The Java Development Kit

The Java Development Kit is key to all of the above. It provides everything we need to make Java applications. In particular, the JDK provides the `javac` command we use to compile Java code.

The JDK also includes the JRE, which provides the `java` command we use to execute our Java bytecode. Many other useful tools are included for debugging, analyzing code, and packaging applications for distribution.

# The Basics

In this section we're going to discuss most basic syntax of the Java programming language.

## Boilerplate

All Java files must follow a specific structure. This is the _syntax_ of Java. At an absolute minimum a Java file must contain this:

```java
class Example {}
```

<!-- demo: create this in compilejava.net -->

This code compiles, but can't be executed yet. To do this we need to add more boilerplate code.

```java
public class Example {
    public static void main(String[] args){
        System.out.println("Hello World!");
    }
}
```

This, you can actually run!

![Output of Example Hello World.png](https://tiy-learn-content.s3.amazonaws.com/0d74569a-Output%20of%20Example%20Hello%20World.png)

<!-- demo: demo this -->

You may be wondering what all this code means. Don't worry about it. You have to understand a bit of Java before you'll be able to really understand this... Java. It's a bit of a chicken or egg problem.

Here's what I _do_ want you to understand:

This chunk of code is called a _class_. Do you see the word `Example`? This tells us this class is called `Example`. Don't worry about what a class is yet.

Do you see the word `main`? `main` is preceded by and followed by gibberish. Let's not worry about the gibberish at this point. All you need to know is that this denotes something called the _main method_.

Everything between the first `{` curly brace after the `main` keyword to the subsequent `}` curly brace is called the method *body*.

Ultimately, every Java application has a main method somewhere. This is the starting point for any Java application. It's what Java executes first when you run your program. For now, let's only focus on the `main` method's body. 

This is the body of the `main` method in our `Example` file:

```java
System.out.println("Hello World!");
```

While we're getting started, this is where we will put our code. 

## Comments

Source code can be inscrutable. Understanding _your own_ code can be challenging, much less someone else's. While your program might make sense to a computer, humans are the ones who have to write and maintain that code. It's essential that we communicate to ourselves and other what exactly we are trying to accomplish. 

_Comments_ denote lines or blocks of text the compiler completely ignores. These are how you leave helpful messages to yourself or others in your source code. 

You can also use comments to _comment out_ chunks of code you don't want to use, but don't want to delete either. 

## Line comments

**Syntax:** `//<your comment>`

Line comments are used to add a comment to a single line of source code. As soon as Java sees `//` it will stop processing anything until the end of that line of text.


```java
public class Example {
    public static void main(String[] args){
    
        // Java will ignore this line.

        // Print out "Hello, world!"
        System.out.println("Hello, world!"); // Java will still process this line, but it will stop as soon as it finds this comment.  

        // int meaningOfLife = 42;
		
    }
}
```

## Block comments

**Syntax:** `/*<your comment>*/`

Block comments are used to add comments that stretch across multiple lines of code. As soon as Java sees `/*` it will stop processing anything until it finds `*/`.

```java
public class Example {
    public static void main(String[] args){
    
        /* 
        This will be ignored
        The contents have no impact
        Share your insights here
        */

        System.out.println("Hello, world!"); 

        /*
        int meaningOfLife = 42;
        int weightPerPigeon = 10;
        */
		
    }
}
```

## Semicolons

Semicolons are extremely important in Java. Every _statement_ must end with a semicolon. A statement is generally a single line of code inside a _block_ of code like the `main` method. The semicolon tells Java that it has reached the end of an statement. 

This code won't compile because the statements inside the main method's body aren't terminated with semicolons:

```java
public class Example {
    public static void main(String[] args){
    
        System.out.println("Hello World!")
		
    }
}
```

This, however, will compile:

```java
public class Example {
    public static void main(String[] args){
    
        System.out.println("Hello World!");
		
    }
}
```

Semicolons may seem like a small detail, but it is a **huge** issue. One of the most common problems <span style="text-decoration:line-through;">new</span> programmers have is forgetting semicolons. 

I hope you like semicolons! 

# Variables

Do you remember basic algebra from middle school? Remember how variables could stand in for numeric values? Variables in Java are the same concept, but they can stand in for other types of data too.

In algebra you might say that `x = 2016`. Now, anywhere you see `x` you can substitute `2016`. That works in Java too. 

```java
public class Example {
    public static void main(String[] args){

		// An example variable
        int x = 2016;
        
		// Anywhere we see "x" we know it means "2016", just like algebra!
		System.out.print(x + 4);
		
    }
}
```

Variables in Java don't need to be single letters like `x`. In Java variable names can be entire words, though there are some important rules you have to follow.

* Variable names are _case sensitive_! A variable named `person` can only be accessed as `person`, not `Person`, `PERSON`, `perSon`, or any other variation.
* Variables can only start with a letter, the underscore character `_`, or a dollar sign `$`. This means that a variable may not start with a number or any other special character.
* Subsequent characters in the variable name can be any combination of letters, numbers, dollar signs, or underscores.

Here are some valid (though mostly terrible) variable names:

* `x`
* `X`
* `person`
* `$system`
* `_______`
* `a`
* `NAME`

Here are some invalid variable names:

* `@username`
* `1thing`
* `\[person\]`
* `something with spaces`

There are some common conventions used when naming variables in Java:

### Give variables meaningful names that are easily understood.

Don't unnecessarily abbreviate or use acronyms. For example, a variable named `delay` is much easier to understand than one named `dly` or `d`. I'd much rather see an excessively long variable name I can easily understand rather than a short one that is inscrutable.

### Variables should either be lower case or [camelCase](https://en.wikipedia.org/wiki/CamelCase).

**Syntax:** `<data type> <variable name>`

In camel case the first letter of a variable is always lowercase. If the variable is made up of multiple words strung together, the first letter of each subsequent word is capitalized.

Here are some good variable names:

* `name`
* `camelCase`
* `grossDomesticProduct`
* `weightPerPigeon`

Here are some bad variable names:

* `NAME`
* `camelcase`
* `gdp`
* `wpp`

In some other languages it is common to separate multiple words with underscore. EG: `gross_domestic_product`. That is not the convention in Java. You will occasionally see variable names that are all upper case where words are separated by underscores, but these are used for a specific purpose. EG: `MAX_VALUE`

## Static Typing

All variables in java are _statically typed_. In other words, you, as the developer, have to explicitly tell Java what type of data a variable stores. Data is any type of information. It could be an audio file, the geographic location of two cities, your own age, weight, and height, or anything else. For now we'll focus on really simply types of data.

When setting a variable in Java you explicitly specify the variable's data type, its name, and, optionally, an initial value. If we wanted to create a variable to hold a simple numeric value we could write.

```java
public class Example {
    public static void main(String[] args){
    
        // create a variable to hold the meaning of life
        int meaningOfLife = 42;
      
      	// output the value of meaningOfLife
      	System.out.println(meaningOfLife);
		
    }
}
```

In this example, `int` tells Java that the variable is an integer; a whole or counting number. We name the variable `meaningOfLife`. The `=` sign tells Java that we're setting the variable to `42`. 

In English this is the same as saying, "Remember that the meaning of life is 42!"

# Primitives

_Primitives_ are the most basic type of data in Java. They are pure, simple, values and serve as building blocks for more complex types of data.

The `int` example above uses the primitive data type of integer. An integer is one of many primitive data types.

The most common primitive data types are:

* **boolean** A value indicating true or false.
* **integer** A whole number.
* **long** A (potentially very big) whole number.
* **double** A (potentially very big) decimal number.
* **char** A single character.

We'll skip over the other primitives. [You can get more details about primitive data types here.](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)

## Boolean

**Keyword:** `boolean`

Booleans are primitive values that indicate _true_ or _false_.

Is 12 greater than 42? `False`.

Is Doug an Iron Yard instructor? `True`.

We can use boolean values to make decisions and control what our application does. For example, we can check to see if a user is logged into our application. If not (`false`) they are sent to a login form. If so (`true`), they may use the application.

```java
public class Example {
    public static void main(String[] args){
    
        boolean skyIsBlue = true;
		boolean oceanIsOrange = false;
		
		System.out.print("The sky is blue: ");
      	System.out.println(skyIsBlue);
      
		System.out.print("The ocean is orange: ");
      	System.out.println(oceanIsOrange);
		
    }
}
```

## Integer

**Keyword:** `int`

Integers represent whole numbers. Whole numbers are the numbers we count with, 1, 2, 3..., etc.

In Java, integers are any whole number from -2,147,483,648 to 2,147,483,647.

_Note: Java's syntax for integers does not allow for commas!_

Here are some example integers:

* -2147483648
* -7836832
* -74
* 0
* 1
* 42
* 90032
* 2147483647

These are _not_ integers:

* -123.456
* 0.57721
* 3.1415
* 4.6692
* 90032.0000000001

```java
public class Example {
    public static void main(String[] args){
    
        int speedLimit = 35;
		int actualSpeed = 47;
		
		System.out.println("The speed limit is: " + 35);
		System.out.println("You were actually going: " + 47);
		
    }
}
```

## Double

**Keyword:** `double`

Doubles represent decimal numbers. Unfortunately, it is difficult to represent decimal numbers precisely in binary. Because of this, doubles are actually _estimates_ of decimal value. This can be a problem when comparing values. We'll come back to this.

Doubles should not be used when doing anything with money. If you need that, take a look at [BigDecimal](https://docs.oracle.com/javase/8/docs/api/java/math/BigDecimal.html).

Doubles can be any number from -9,223,372,036,854,775,808 (very small) to 9,223,372,036,854,775,807 (exceptionally large). Again, you can't actually use commas in Java numbers.

Here are some example doubles:

* -2147483648
* -7836832
* -123.456
* -74
* 0
* 0.57721
* 1
* 3.1415
* 4.6692
* 42
* 90032
* 90032.0000000001
* 2147483647

You can add a "d" onto the end of a number to explicitly differentiate doubles from integers:

* 0.57721d

or

* 90032d

```java
public class Example {
    public static void main(String[] args){
    
        double pi = 3.1415926535;
		double weight = 190d;

      	System.out.println("Pi to 10 digits is: " + pi);
      	System.out.println("This thing weighs " + weight + " pounds.");
    }
}
```

Double are sometimes called _floating point numbers_. 

## Char

**Keyword:** `char`

A char represents a single character. For example:

* a
* Z
* 9
* @
* ë
* ß

```java
public class Example {
    public static void main(String[] args){
    
        char theFirstLetter = 'a';
        char theLastLetter = 'Z';
		char ampersand = '&';
		
      	System.out.println("These chars are: " + theFirstLetter + " " + ampersand + " " + theLastLetter);
      
    }
}
```

As you can imagine, a single character has limited utility. We'll need to find a way to collect a sets of characters together to form words and sentences. These are called strings and we'll get to them in a bit.

## Null

**Keyword:** `null`

Null is not actually a type of data. Null is the absence of value. It is not zero. It is not anything. It is the black hole of values.

Null can be used to tell Java that there is no value for a variable. For example, what is the address of a homeless person? Null. They have no address.

<!-- todo: see if the class can come up with their own examples of null -->

```java
public class Example {
    public static void main(String[] args){
    
        String address = null;
		
      	System.out.println(address);
    }
}
```

[The inventor of null, Tony Hoare, calls it his billion-dollar mistake.](https://www.lucidchart.com/techblog/2015/08/31/the-worst-mistake-of-computer-science/)

# Operators

![hello operator.jpg](https://tiy-learn-content.s3.amazonaws.com/910fb126-hello%20operator.jpg)

Operators are used to manipulate data. They can act on one, two, or even three individual values. They might modify the data directly or produce an entirely new value that we can work with.

[The full set of Java operators can be seen here.](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/opsummary.html)

## Assignment Operator

**Operator:** `=`

**Syntax:** `<Variable to set> = <Value to assign to the variable>`

We've already seen the assignment operator. The assignment operator is used to set the value of a variable. The variable being set is to the left of the `=` operator. The value to use is to the right of the `=` operator.

```java
public class Example {
    public static void main(String[] args){
    
        boolean skyIsBlue = true;
		boolean oceanIsOrange = false;
		
		System.out.println("The sky is blue: " + skyIsBlue);
		System.out.println("The ocean is orange: " + oceanIsOrange);
		
    }
}
```

Because Java is statically typed, you must always be sure to only assign values to variables of the same type. For example, you can't set a boolean variable to `'c'`.

```java
public class Example {
    public static void main(String[] args){

		// this doesn't work!
        boolean skyIsBlue = 'c';
		boolean oceanIsOrange = false;
		
		System.out.println("The sky is blue: " + skyIsBlue);
		System.out.println("The ocean is orange: " + oceanIsOrange);
		
    }
}
```

That said, there are some places where Java will automatically convert data types for you. For example, you can set a double variable to an integer value. Java will simply convert the integer to a double for you. This is called _widening_. The reason this can be done is that a double can contain all the information in an integer and more.

```java
public class Example {
    public static void main(String[] args){
    
      	// let's make an int
      	int weightAsInt = 190;
      
      	// let's make a double, but set it to an int
		double weightAsDouble = weightAsInt;

      	// hey look, the double became an int!
      	System.out.println("This thing weighs " + weightAsDouble + " pounds.");
    }
}
```

[If you're having trouble sleeping, consider reading more about conversions and promotions in Java.](https://docs.oracle.com/javase/specs/jls/se7/html/jls-5.html)

## Arithmetic Operators

Computers excel at arithmetic. After all, that's what they're designed to do!

### Addition Operator

**Operator:** `+`

**Syntax:** `<a value> + <another value>`

**Returns:** The sum of the two values.

The addition operator adds two values together. The value to the left of the `+` sign is added to the value on the right. The resulting value is _returned_. This works more or less as you would think it should.

```java
public class Example {
    public static void main(String[] args){
    
      	int dozen = 4 + 8;
      
      	System.out.println("A dozen is " + dozen + " things.");
      	
      	// Note: this doesn't work as expected without the parenthesis around "dozen + 1". Any ideas why?
      	// Hint: It has something to do with algebra. Think about PEMDAS. 
      	// Another Hint: It also has something to do with handling different data types.
      	System.out.println("A baker's dozen is " + (dozen + 1) + " things.");
    }
}
```

The above example shows that you can combine two or more operators in a single _expression_. Remember that the `=` operator assigns the value on the right into the variable on the left. Logically, Java has to _evaluate_ the value on the right first. The result of that evaluation is what the `=` operator assigns into the variable.

You should also take note that the result of adding 4 to 8 is an integer value. The variable we're setting is also an integer. We always have to be thinking about data types.

### Subtraction Operator

**Operator:** `-`

**Syntax:** `<a value> - <another value>`

**Returns:** The difference of the two values.

Similar to the addition operator, the subtraction operator subtracts the value to the right of the `-` symbol from the value on the left and returns the result.

```java
public class Example {
    public static void main(String[] args){
    
      	int bottlesOfBeerOnTheWall = 99;
      	int quantityToTakeDown = 1;
      	int remainingBottlesOfBeerOnTheWall = bottlesOfBeerOnTheWall - quantityToTakeDown;
      
      	System.out.println(bottlesOfBeerOnTheWall + " bottles of beer on the wall,");
      	System.out.println(bottlesOfBeerOnTheWall + " bottles of beer!");
      	System.out.println("Take " + quantityToTakeDown + " down,");
      	System.out.println("pass it around!");
      	System.out.println(remainingBottlesOfBeerOnTheWall + " bottles of beer on the wall!");
      	
    }
}
```

### Multiplication Operator

**Operator:** `*`

**Syntax:** `<a value> * <another value>`

**Returns:** The product of the two values.

The multiplication operator multiplies the value to the left of the `*` operator by the value on the right and returns the result.

```java
public class Example {
    public static void main(String[] args){
    
		int rocksInABox = 9;
      	double rockWeight = 2.34; // pounds
      	double boxWeight = rocksInABox * rockWeight;
      
      	System.out.println("This box of " + rocksInABox + " rocks weighs " + boxWeight + " pounds.");          
    }
}
```

### Division Operator

**Operator:** `/`

**Syntax:** `<a value> / <another value>`

**Returns:** The quotient of the two values.

The division operator divides the value to the left of the `/` symbol by the value on the right and returns the result.

```java
public class Example {
    public static void main(String[] args){
    
		int rocksInABox = 9;
      	double boxWeight = 21.06;
      	double averageWeightOfRock = boxWeight / rocksInABox;
      
      	System.out.println("The average weight of a rock in this box is " + averageWeightOfRock + " pounds.");          
    }
}
```

Division is an interesting beast as far as types are concerned. Consider this example:

```java
public class Example {
    public static void main(String[] args){
      
      	double x = 3/2;
      
		System.out.println(x);          
    }
}
```

You might expect that `3/2` would return `1.5`, a double, but it doesn't. It actually returns `1`! This is because the _operands_, `3` and `2`, are integers, not doubles. If at least one of the operands is a double, then the result will be a double.

```java
public class Example {
    public static void main(String[] args){
      
      	double x = 3d/2;
      
		System.out.println(x);          
    }
}
```

Keep in mind that this behavior with integers may actually be useful. For example, imagine you run a breakfast restaurant serving omelets. Each omelet requires 3 eggs and you have 116 eggs total. How many people can you feed?

```java
public class Example {
    public static void main(String[] args){
      
      	int eggsPerOmelet = 3;
      	int numberOfEggs = 116;
      	int maxOmelets = numberOfEggs/eggsPerOmelet;
      
		System.out.println("You can make " + maxOmelets + " omelets!");          
    }
}
```

According this this, you can feed 38 customers. A nice round integer like 38 is much more useful than 38.666666666666664, since we can't feed two thirds of a person. Granted, we could round this down, but that's another step, and not something you know how to do yet.

<!-- todo: ask the class why there's a 4 at the end of 38.666666666666664 -->

You can't divide an integer by zero, but you can divide a double by zero. 

### Remainder operator

**Operator:** `%`

**Syntax:** `<a value> % <another value>`

**Returns:** The remainder when dividing the two values.

Remember long division from elementary school?

![Long division - the bane of 4th graders everywhere.](https://tiy-learn-content.s3.amazonaws.com/2095fdec-long%20division.gif)

The remainder operator, often called the modulo operator, returns the remainder when dividing the value to the left of the `%` symbol by the value to the right.

Going back to the omelet example, perhaps you want to know how many eggs will be left over if you sell all of your omelets?

```java
public class Example {
    public static void main(String[] args){
      
      	int eggsPerOmelet = 3;
      	int numberOfEggs = 116;
      	int eggsRemaining = numberOfEggs % eggsPerOmelet;
      
		System.out.println("After making all your omelets you will have " + eggsRemaining + " eggs remaining.");
	}
}
```

## Unary operators

Unary operators work with only one operand. Some unary operators modify the operand itself, others simply return the result of the operation.

### Unary increment

**Operator:** `++`

**Syntax:** `<a variable>++` or `++<a variable>`

**Returns:** It depends...

The unary increment operator is used to add 1 to a variable. This example shows how a variable `x` is incremented. The result of this is that `x` becomes 124.

```java
public class Example {
    public static void main(String[] args){
      
      	int x = 123;
		System.out.println("x is " + x);
      
		x++;
		System.out.println("x is now " + x);
	}
}
```

The `++` symbol can be placed before or after a variable. However, the location of the operator changed its behavior subtly. This is because the unary increment operator doesn't only modify the variable being incremented, it also returns one of two values, depending on where the operator is placed.

Placing the operator after the variable increments the variable and returns the value of the variable _before_ it is incremented.

```java
public class Example {
    public static void main(String[] args){
      
      	int x = 123;
		System.out.println("x is " + x);
      
      	int y = x++;
      
		System.out.println("y is " + y); // maybe not what you'd expect.
		System.out.println("x is now " + x);
	}
}
```

You can read the last line of this sample as, "set `y` to the value of `x`, then increment `x` by 1." In this example `x` becomes 124 and `y` becomes 123.

Placing the operator before the variable causes the variable to be incremented _before_ the new value is returned.

```java
public class Example {
    public static void main(String[] args){
      
      	int x = 123;
		System.out.println("x is " + x);
      
      	int y = ++x;
      
		System.out.println("y is " + y); // probably what you'd expect.
		System.out.println("x is now " + x);
	}
}
```

You can read the last line of this sample as, "increment x by 1 and then set y to the value of x." In this example both `x` and `y` become 124.

### Unary decrement

**Operator:** `--`

**Syntax:** `<a variable>--` or `--<a variable>`

**Returns:** It depends...

Similar to the unary increment operator, the unary decrement operator subtracts 1 from a variable.

```java
public class Example {
    public static void main(String[] args){
      
      	int x = 123;
		System.out.println("x is " + x);
      
		x--;
		System.out.println("x is now " + x);
	}
}
```

In this example `x` becomes 122.

As with the unary increment operator, the placing the `--` operator before the variable returns the result after the variable has been decremented. Placing the `--` operator after the variable returns the variable before it is decremented.

### Unary negation

**Operator:** `-`

**Syntax:** `-<a variable or value>`

**Returns:** A negated value.

Just like in math, you use the negation operator to denote negative numbers.

```java
public class Example {
    public static void main(String[] args){
      
      	int x = -123;
		System.out.println("x is " + x);
      
	}
}
```

It can also be used to negate values, again, just like it math. The negative of a negative is positive.

```java
public class Example {
    public static void main(String[] args){
      
      	int x = -123;
      	
      	// y is the negative value of x. A negative negative is a positive.
		int y = -x;
      
		System.out.println("x is " + x);
		System.out.println("y is " + y);
      
	}
}
```

In this example `y` becomes 123.

## Comparison Operators

Very often we need to compare values. Java provides a set of operators we can use to compare two values.

### Equality Operator

**Operator:** `==`

**Syntax:** `<a boolean value> == <another boolean value>`

**Returns:** True if the value on the left is equal to the value on the right.

The equality operator `==` is simple, it just checks to see if two values are the same. If so, true; if not, false.

```java
public class Example {
    public static void main(String[] args){
      
      	System.out.println(5 == 5);
		System.out.println(5 == 6);
      
	}
}
```

Since 5 does, in fact, equal 5 the first line evaluates to true. However, since 5 is not 6, the second line evaluates to false.

Be sure to note that the equality operator, `==`, is completely different from the assignment operator, `=`. The former checks to see if two values are equal while the latter sets the value of a variable. It is a common error to accidentally use the assignment operator when you mean to use the equality operator.

<!-- todo: demonstrate that you can't write code like 5 = 5 -->

### Inequality Operator

**Operator:** `!=`

**Syntax:** `<a boolean value> != <another boolean value>`

**Returns:** True if the value on the left is _not_ equal to the value on the right.

The inequality operator `!=` is the exact opposite of the equality operator, it checks to see if two values are different. If different, true; if the same, false.

```java
public class Example {
    public static void main(String[] args){
      
		System.out.println(5 != 5);
      	System.out.println(5 != 6);
      
	}
}
```

Since 5 doesn't equal 6 the first line evaluates to true. However, since 5 is the same as 5, the second line evaluates to false.

### Greater Than Operator

**Operator:** `>`

**Syntax:** `<a boolean value> > <another boolean value>`

**Returns:** True if the value on the left is greater than the value on the right.

```java
public class Example {
    public static void main(String[] args){
      
		System.out.println(5 > 5);
      	System.out.println(5 > 6);
      	System.out.println(6 > 5);
      
	}
}
```

### Less Than Operator

**Operator:** `<`

**Syntax:** `<a boolean value> < <another boolean value>`

**Returns:** True if the value on the left is less than the value on the right.

```java
public class Example {
    public static void main(String[] args){
      
		System.out.println(5 < 5);
      	System.out.println(5 < 6);
      	System.out.println(6 < 5);
      
	}
}
```

### Greater Than Or Equal To Operator

**Operator:** `>=`

**Syntax:** `<a boolean value> >= <another boolean value>`

**Returns:** True if the value on the left is greater than or equal to the value on the right.

```java
public class Example {
    public static void main(String[] args){
      
		System.out.println(5 >= 5);
      	System.out.println(5 >= 6);
      	System.out.println(6 >= 5);
      
	}
}
```

### Less Than Or Equal To Operator

**Operator:** `<=`

**Syntax:** `<a boolean value> <= <another boolean value>`

**Returns:** True if the value on the left is less than or equal to the value on the right.

```java
public class Example {
    public static void main(String[] args){
      
		System.out.println(5 <= 5);
      	System.out.println(5 <= 6);
      	System.out.println(6 <= 5);
      
	}
}
```

### Comparison Operators Notes

Be aware that comparison operators can only be used with two values, the value to left of the operator and the value to the right of the operator. Whereas in math we can write ` 1 < x < 10`, that will result in an error in Java.

## Logical Operators

So far we've seen how to modify, combine, and compare values using arithmetic, unary, and comparison operators. Now we need to learn how to make decisions accordingly.

Logical operators return boolean true or false values. We can use these to control how our programs behave.

### Logical And

**Operator:** `&&`

**Syntax:** `<a boolean value> && <another boolean value>`

**Returns:** True if both boolean values provided are true, otherwise false.

In programming you will often want to make decisions based on one or more conditions. For example, among other criteria, [NASA will only launch a rocket if](http://www.nasa.gov/centers/kennedy/news/releases/2003/release-20030128.html) the wind speed is below 42 knots and the sky is clear. This can be expressed using the logical and operator.

```java
public class Example {
    public static void main(String[] args){
      
		double currentWindSpeed = 26.4;

        boolean windSpeedOk = currentWindSpeed < 42;
        boolean skyIsClear = true;

        boolean goForLaunch = windSpeedOk && skyIsClear;
      
      	System.out.println("Go for launch?: " + goForLaunch);
      
	}
}
```

In this example we determine that we are go for launch because the wind speed is below the allowed threshold and the sky is clear.

However, if the wind speed is too high, the sky isn't clear, or both, then the `goForLaunch` would be false.

### Logical Or

**Operator:** `||`

**Syntax:** `<a boolean value> || <another boolean value>`

**Returns:** True if either or both boolean values are true, false if both values are false.

The logical or operator is similar to the "and" operator, but is only false if both operands are false.

```java
public class Example {
    public static void main(String[] args){
      
		boolean iWantTea = false;
      	boolean iWantCoffee = true;
      
      	boolean iWantAWarmBeverage = iWantTea || iWantCoffee;
      
      	System.out.println("Do I want a warm beverage?: " + iWantAWarmBeverage);
      
	}
}
```

### Logical Not

**Operator:** `!`

**Syntax:** `!<a boolean value or variable>`

**Returns:** The opposite of the boolean value provided.

In English the word "not" negates what comes next. The not operator in Java does the same thing. Essentially you can make something not-true or not-false using the `!` operator.

```java
public class Example {
    public static void main(String[] args){
      
		boolean oppositeOfTrue = !true;
        boolean oppositeOfFalse = !false;
      
      	System.out.println("The opposite of true is " + oppositeOfTrue);
      	System.out.println("The opposite of false is " + oppositeOfFalse);
      
	}
}
```

## Other Operators

There are a number of other operators we haven't covered because they're not important at this point. You can [read more on Java operators here](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/operators.html).

# Conditionals

Essentially, all software begins executing on the first line and continues until it reaches the last line. It's sort of like the script for a play: Romeo says something, Juliette says something, they both die, end of story. 

Actually, it's a bit more complex than that. It's more like one of those interactive dinner theaters. There's one script, but it branches depending on who the audience decides the murderer is.

I think of conditionals like a series of dams on a river. They control and redirect the flow of the river.

In programming, we use conditional logic to control this flow. Conditions are criteria that must be met for a block of code to be executed. For example:

* Did the user push the jump button? 
	* If so: Then make the character jump.
	
*  Is is the temperature in the refrigerator higher than 34 degrees?
	* If so: Turn on the cooling unit. 

* Has the user filed their TPS report today?
	* If so: 
		* Thank them for being such a valued employee.
	* If not:
		* Nag them.

## If statements

**Syntax:**

```Java
if(<conditional expression that evaluates to true>){
	<block of code>
}
```

An `if` statement executes a _block_ of code only if a conditional expression evaluates to true. Blocks of code are the lines of code between curly braces.

Remember the logical operators we just discussed? This is where they really come into play. For example:

```java
public class Example {
    public static void main(String[] args){

        boolean milk = true;
        boolean cream = false;
        boolean soyMilk = false;

        boolean caffeinatedEspresso = true;
        boolean decaffeinatedEspresso = false;

        boolean darkChocolate = true;
        boolean lightChocolate = false;

        if( (milk || cream || soyMilk) &&
                (caffeinatedEspresso || decaffeinatedEspresso) &&
                (darkChocolate || lightChocolate) ){
            System.out.println("This is a mocha!");
        }
    }
}
```

Note that the parenthesis control the order of operations, grouping chunks of the expression into single logical units. For example, by itself, `(milk || cream || soyMilk)` evaluates to true because `milk` is true. `(caffeinatedEspresso || decaffeinatedEspresso)` is true because `caffeinatedEspresso` is true. And, `(darkChocolate || lightChocolate)` is true because `darkChocolate` is true. Ultimately we get `true && true && true` which evaluates to true.

## Else statements

**Syntax:**

```Java
if(<conditional expression that evaluates to true>){
	<block of code>
} else {
	<a different block of code>
}
```

Sometimes you want to do one thing or something else. Maybe you want steak or chicken. Usually you don't want both. 

An `else` statement can be tacked onto the end of an if statement. The block of code enclosed in the curly braces after the `else` statement are only executed if the original conditional statement is false.

```java
public class Example {
    public static void main(String[] args){
      
		boolean milk = true;
        boolean cream = false;
        boolean soyMilk = false;

        boolean caffeinatedEspresso = false;
        boolean decaffeinatedEspresso = false;

        boolean darkChocolate = false;
        boolean lightChocolate = false;

        if( (milk || cream || soyMilk) && 
                (caffeinatedEspresso || decaffeinatedEspresso) &&
                (darkChocolate || lightChocolate) ){
            System.out.println("This is a mocha!");
        } else {
            System.out.println("I don't know what this is, but it's not a mocha!");
        } 
      
	}
}
```

## Else If statements

**Syntax:**

```Java
if(<conditional expression that evaluates to true>){
	<block of code>
} else if(<different true conditional expression>){
	<another block of code>
} else {
	<a different block of code>
}
```

Often you will want to make decisions based on more than only one conditional statement. In this case you can use _else if_ statements. 

Java will evaluate the first `if` statement. If that's false, it will check the next `else if` statement. If that's false, it will continue checking `else if` statements until one evaluates to `true`. If none of them evaluate to `true` the else `block` (if provided) will be executed, if provided. Only one block of code in the entire statement can be executed. 

```java
public class Example {
    public static void main(String[] args){
      
		boolean milk = true;
        boolean cream = false;
        boolean soyMilk = false;

        boolean caffeinatedEspresso = false;
        boolean decaffeinatedEspresso = false;

        boolean darkChocolate = false;
        boolean lightChocolate = false;

        // is this a mocha?
        if( (milk || cream || soyMilk) && 
                (caffeinatedEspresso || decaffeinatedEspresso) &&
                (darkChocolate || lightChocolate) ){
            System.out.println("This is a mocha!");

        // is this a latte?
        } else if( (milk || cream || soyMilk) && 
                (caffeinatedEspresso || decaffeinatedEspresso) &&
                !(darkChocolate || lightChocolate) ) {
            System.out.println("This is a latte!");

        // is this just milk?
        } else if(milk && !cream && !soyMilk && 
                !caffeinatedEspresso && !decaffeinatedEspresso &&
                !darkChocolate && !lightChocolate ) {
            System.out.println("This is just milk!");

        // who knows what the heck this is...
        } else {
            System.out.println("I don't know what this is.");
        } 
      
	}
}
```

Take particular note of the order of the `if` and `else-if` statements. If we put the latte conditional first we would never reach the mocha conditional. This is because a mocha is just a latte, but with chocolate. 

Be sure to carefully consider what order your `if`, `else if`, and `else` blocks are written.

# Loops

Computers were invented to do repetitive tasks, something humans are really bad at. Have you ever lost count of something? Have you forgotten your place in a long list? Java won't do that.

There are a few ways to loop over data in Java. We'll touch on three of them here.

## For loop

**Syntax:** 

```java
for(<initializing expression> ; <conditional expression> ; <afterthought expression> ){
	<body to loop over>
}
```

`For` loops seem complicated on the surface, but they're actually pretty simple. Typically, what we're telling Java is that we're going to loop from one value, to another value, stepping incrementally through each iteration through the loop.

Let's break down an example `for` loop:

```java
public class Example {
    public static void main(String[] args){
      
		for(int x = 0 ; x <= 10 ; x++){
            System.out.println(x);
        } 
      
	}
}
```

We'll focus in on the first line of code first. The `for` keyword simply tells Java that this is a `for` loop. Inside the parenthesis we have three  distinct expressions separated by semicolons. 

* **Initializing expression:** `int x = 0`
	This tells Java we're starting the loop with a variable named `x` set to 0.

* **Conditional expression:** `x <= 10`
	This tells Java to keep looping so long as `x` is less than or equal to 10.

* **Afterthought expression:** `x++`
	Increment `x` by after each iteration trough the loop.

Putting this together, our example loop follows this flow:

1. **Initialization:** Define a variable named `x` and set its value to `0`.

2. **Conditional:** Is `x` less than or equal to `10`? Yes.
3. **Body:** Output `0` to the console.
4. **Afterthought:** Increment `x`, setting it to `1`.

5. **Conditional:** Is `x` less than or equal to `10`? Yes.
6. **Body:** Output `1` to the console.
7. **Afterthought:** Increment `x`, setting it to `2`.

8. **Conditional:** Is `x` less than or equal to `10`? Yes.
9. **Body:** Output `2` to the console.
10. **Afterthought:** Increment `x`, setting it to `3`.

	... ect, etc ...

31. **Afterthought:** Increment `x`, setting it to `10`.

32. **Conditional:** Is `x` less than or equal to `10`? Yes.
33. **Body:** Output `10` to the console.
34. **Afterthought:** Increment `x`, setting it to `11`.

35. **Conditional:** Is `x` less than or equal to `10`? No.

And, we're done with our loop.

It's worth noting at all three of the expressions in the for loop are optional and can be left blank.

<!-- demo: an infinte loop -->

## While loop

**Syntax:** 

```java
while(<conditional expression>){
	<body to loop over>
}
```

`While` loops are similar to `for` loops, but they only have a single conditional expression. The conditional expression in a `while` loop is executed before each execution of the body. 

Here's an example `while` loop that does the same thing as the `for` loop above:

```java
public class Example {
    public static void main(String[] args){
      
		int x = 0;
        while(x <= 10){
            System.out.println(x);
            x++;
        }
      
	}
}
```

Note that in this example we defined our own variable that is an equivalent to the initializing variable in the `for` loop example. We also increment it at the end of the `while` loop's body, just like we did in the afterthought expression in the `for` loop. We don't _need_ to do this, per se, all we need is the conditional expression after the `while` keyword.

Abbreviated, our logic looks like this:

1. Is `x` less than or equal to 10? Yes
2. Output `x` and increment it to 1.
3. Is `x` less than or equal to 10? Yes
4. Output `x` and increment it to 2.
5. Is `x` less than or equal to 10? Yes
6. Output `x` and increment it to 3.

... ect, etc ...

22. Is `x` less than or equal to 10? Yes
23. Output `x` and increment it to 11.
24. Is `x` less than or equal to 10? No.

And, we're done with our loop.

You should note that the conditional expression is evaluated before and after each iteration through the loop.

In general `while` loops are a lot less common than `for` loops.

## Do while loop

**Syntax:** 

```java
do{
	<body to loop over>
} while(<conditional expression>);
```

The `do while` loop is almost identical to the `while` loop, except that the conditional expression is only evaluated at the end of the loop. The body of the loop is always executed at least once. If the conditional expression evaluates to `true` the loop is run again. This continues until the conditional expression evaluates to `false`.

Here's the same loop from 0 to 10, but in `do while` form:

```java
public class Example {
    public static void main(String[] args){
      
		int x = 0;

        do{
            System.out.println(x);
            x++;
        } while(x <= 10);
      
	}
}
```

One thing to note is that if `x` were any value at all, this expression would always output it once. For example:

```java
public class Example {
    public static void main(String[] args){
      
		int x = 15;

        do{
            System.out.println(x);
            x++;
        } while(x <= 10);
      
	}
}
```

This will output `15` to the console one time, but will not loop since `15` is greater than `10`.

This is probably the least common form of looping in Java. I don't recommend using it unless you have a good reason.

## Nested loops

The last thing to note about loops - or really any other blocks of code in Java - is that they can be _nested_ within each other. For example, we could output a times table like this:

```java
public class Example {
    public static void main(String[] args){
      
		for(int x = 1 ; x <= 12 ; x++){

            // print out the columns in this row of the times table
            for(int y = 1 ; y <= 12 ; y++){

                // calculate the product
                int product = x * y;

                // output the product
                System.out.print(product + " ");

            }

            // start a new line
            System.out.print("\n");
        }
      
	}
}
```


Classes and Objects

# Classes

A class is a type of data that can hold other types of data. Pretty much everything in Java is made up of classes. 

In programming, we use classes to model real world and abstract concepts. A class can be used to describe a type of _object_, it's properties, and whatever it can do. 

A class is like a blueprint for a house. A blueprint is a detailed plan for building a house. It shows the placement and measurements of all rooms, where fixtures will be placed, where utilities will be run, how the roof will be assembled, and much, much more. 

![House_Plans_(Blueprints).jpg](https://tiy-learn-content.s3.amazonaws.com/b9067c2c-House_Plans_%28Blueprints%29.jpg)

An object is like a house you built using the blueprint. You can make many houses using the same blueprint, but each house is distinct.

![what a house might look like.jpg](https://tiy-learn-content.s3.amazonaws.com/70364e47-what%20a%20house%20might%20look%20like.jpg)

Remember our original hello world program?

```java
public class Example {
    public static void main(String[] args){
        System.out.println("Hello World!");
    }
}
```

In this example we wrote a class named `Example`. The `Example` class doesn't have any properties to describe it, but it does have one method we can use to interact with it, the `main` method. This main method is _invoked_ when we execute the program.

Classes are pervasive in Java. The example above uses several classes other than the `Example` class itself.

* `String[]` - This is actually two classes, String and Array.
* `System` - The system class. It has system-specific behaviors and properties.
* `"Hello World!"` - Another String.
* `Object` - All classes are derived from this class.

## Objects

If a class in Java is a blueprint, then what you build from that blueprint is called an _object_.

Classes are to blueprints as objects are to houses. This is a topic that often confuses new programmers.

A blueprint doesn't provide much shelter or storage space; it doesn't _do_ much of anything other than tell us how to build a house. It's essentially _metadata_; data that describes other data.

On the other hand, a house _does_ provide shelter and storage space. However, it doesn't tell you how to build another house. 

A class doesn't do the "magic bits" (not a technical term). You have to use the class to create an object that does do the magic bits.

## String literals

**Syntax:** `"<some text>"`

`String` is a class that represents a collection of letters. In english, this is what you use to make bits of text like words, sentences, paragraphs, or the next great american novel. (I don't recommend the latter.)

Strings are unique in Java in that they have a _string literal_ syntax. Java automatically recognizes that the characters contained between double quotes represent a `String` object. 

We've already used strings throughout this class:

```java
public class Example {
    public static void main(String[] args){
        System.out.println("Hello World!");
    }
}
```

In this familiar example, `"Hello World!"` is a string. More accurately, `"Hello World!"` is an _instance_ of a string expressed in string literal syntax. The process of creating an instance of a class is called _instantiation_. You instantiate instances of classes. In this case we're instantiating an instance of a string using string literal syntax.

The etymology of "instantiate" may be helpful to understand:

* **īnstantia** Latin. 
	1. a being near, presence

* **-ate** Latin suffix
	1. (in adjectives) having the specified thing
	2. (in adjectives) characterized by the specified thing
	3. (in adjectives) resembling the specified thing

So, the verb instantiate is the act of having a specified object present. 

Remember how classes describe objects? The `String` class describes string objects. `"Hello World!"` is an instance of the String class. `"Insert deep thought here..."` would also be an instance of a string. `"This is an instance of a string."` is too.

## Method invocation

**Syntax:** `<return value> = <instance of an object>.<method name>(<zero or more method arguments>)`. 

In the real world, a string of text has numerous properties you could use describe it. It has a given number of characters. These characters are in specific positions. A string of text might contain another string of text.

Similarly, Strings in Java have several properties and methods for accessing them. For example, the `String` class has a method `length()` that we can use to get the number of characters in a string. Behind the scenes, the String class is just a chunk of code that some other programmer wrote a long time ago. The String class's `length()` method is just a specific subset of the String class' code. 

When we can use the syntax shown above to _invoke_ the String class's `length()` method. When we invoke a method we're telling the String class to execute that specific chunk of code and tell us the results of running that code.

The etymology of invoke may be helpful in understanding this:

* **in-** Latin prefix. 
	1. Prefixed to certain words to give the senses of in, into, towards, within.
* **vocare** Italian
	1. (transitive) to call, name

So, the verb invoke means to call into code within a class.

Oftentimes you hear people refer to _calling_ or _running_ a method. This is just shorthand for invoking. It's perfectly ok to use this language, but I encourage you to be explicit and try to use the word invoke instead.

Let's dig into a few methods of the String class by looking at the string "No pain, no gain".

Remember that Java recognizes the string literal "No pain, no gain" and creates an instance of a String object. We could invoke the `length()` method on this instance object as follows.

@todo
```java
public class Example {
    public static void main(String[] args){
    
      	String message = "No pain, no gain";
        int length = message.length();
      
      	System.out.println("The message \"" + message + "\" is " + length + " characters long."); 
    }
}
```

This sample indicates that there are 16 characters in "No pain, no gain", which is correct!

Take note that the syntax for creating a String variable is the same as creating other types of variable. Once we have our String instance we can invoke methods on the object. We create a new variable of type  `String` and name it `message`. The value of `message` is set by the assignment operator to an instance of the `String` class whose text is `"No pain, no gain"`. 

On the second line we take our new `String` instance and invoke its `length()` method. You should take note that I used the word "its" to denote that our `String` object (an instance of the String class) has its own `length()` method. 

In the same way that two houses built from the same blueprint don't share a single kitchen sink, each object instantiated from a class gets its own methods. 

```java
public class Example {
    public static void main(String[] args){
    
      	String noPain = "No pain, no gain";
        int noPainLength = noPain.length();
        System.out.println(noPain  + ": " + noPainLength);

        String lotaPain = "Lots of pain, lot of gain";
        int lotaPainLength = lotaPain.length();
        System.out.println(lotaPain  + ": " + lotaPainLength);
    }
}
```

This example shows two `String` variables, `noPain` and `lotaPain`. Each of these `String` objects have their own `length()` method. When invoked, these methods return the length of their respective strings.

Another notable method on the String class is substring(). Unlike the length() method, the substring() method accepts two arguments, beginIndex, and endIndex. These tell the method to find the substring of text starting from the beginIndex and continuing to (but not including) the endIndex. The substring() returns this text as a new String object.

```java
public class Example {
    public static void main(String[] args){
    
      	String deepThought = "No pain, no gain";
		System.out.println( deepThought.substring(3, 11) );
    }
}
```

![no pain no gain substring.png](https://tiy-learn-content.s3.amazonaws.com/53697f9f-no%20pain%20no%20gain%20substring.png)

[You can find the full documentation for the String class here.](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)

## New

**Syntax:** `<new object instance> = new <name of class>(<constructor arguments>)`

The `new` keyword is what you use when you're creating a new instance of an object without using literal syntax. Since String is a class, we don't _have_ to use the String literal syntax. We could use the `new` keyword.

```java
public class Example {
    public static void main(String[] args){
    
      	String emptyString = new String();
    }
}
```

This creates a new string object. It's the equivalent to this:

```java
public class Example {
    public static void main(String[] args){
    
      	String emptyString = "";
    }
}
```

Let's try this with a different class, Date. It should be noted that the Date class is _deprecated_. This means it's slated to be removed from Java in the future and shouldn't be used for new code. But, it's an easy class to use and is good for a demo.

```java
import java.util.Date;
 
public class Example {
    public static void main(String[] args){
    
      	Date rightNow = new Date();
		System.out.println( rightNow );
    }
}
```

There's a few new things here that we haven't seen before. At the very top we have `import java.util.Date;`. This tells Java we want to use the `Date` class. Classes in Java are sorted into `packages`. The Date class is in `java.util` package, which we need to specify as a part of the import statement.

In the body of the main method we have `Date rightNow = new Date();`. To the left of the `=` assignment operator we declare a variable named `rightNow` that is of type `Date`. 

To the right of the assignment operator we have `new Date()`. The keyword `new` tells Java we're instantiating a new object. `Date` tells Java the type (IE: the class) of object we're creating. 

The parenthesis tell Java to call a _constructor_ on the new Date object. A constructor is a special method on an object that is called when the object is instantiated. Constructors are defined by the class. A constructor is used to configure an object before it's used. 

In the above example we're calling a constructor that accepts no arguments. This constructor cause the new `Date` object to use the current date and time as its value. The Date class has several constructors, but since they're deprecated they don't work with compilejava.net. 

Here's an example using the deprecated constructor `Date(int year, int month, int date, int hrs, int min)` and another deprecated method, `getYear()` that returns the year from the date.

```java
import java.util.Date;

public class Example {
    public static void main(String[] args){

        Date birthday = new Date(1977, 11, 9, 5, 54);
        System.out.println("Born in year: " + birthday.getYear());

    }
}
```

# Writing classes

Now that we know what classes are, how to instantiate them, and how to call methods on them, let's learn how to actually write our own classes.

## Class

**Syntax:**

```java
<access modifier> class <Class name>{
	<body of class>
}
```

The syntax described above is not exhaustive, but it will do for now. We're going to start out with only the most basic of classes and build up to much more complex classes as we move through our material. The syntax shown above is very minimal and focused on what we care about right now.

You might remember that the very first class we saw this:

```java
class Example {}
```

This class has no access modifier and no body, but it is entirely valid. Because there is no access modifier, only classes in the same directory can instantiate this class.

Since classes are supposed to represent concepts, let's make a class that models a person. Let's start our person model with the most minimal code required:

```java
public class Person {}
```

Note that `Person` is capitalized. It is _convention_ in Java to capitalize class names. Don't be "that person" who doesn't capitalize their class names.

I gave the Person class a `public` access modifier. This access modifier tells Java that other Java code is allowed to instantiate this class.

Let's create another class with a `main` method. We can use this to test our `Person` class as we go along.

```java
public class Main {
    public static void main(String[] args){
        Person doug = new Person();

		System.out.println(doug);
    }
}
```

In this example we're creating a new variable of type `Person`. The variable's name is `doug` and we're assigning a new instance of a `Person` object to that variable. We're also outputting Java's own string representation of the variable to the console. The output looks something like this:

> Person@511d50c0

The first part of the output is the class name. The second part, after the `@`, is the hash code of this object instance. The hash code uniquely identifies this instance of this class. Each time you run this program you will get a different hash code.

### Instances

```java
public class Main {
    public static void main(String[] args){
        Person doug = new Person();
        Person liz = new Person();

		System.out.println(doug);
		System.out.println(liz);
    }
}
```

Here we have added a second instance of the Person object. Note that the output shows this:

> Person@511d50c0
> Person@60e53b93

The hash code for these two objects are different because they are different instances of the object. In your computer's memory, these two objects are sitting in different places. 

We can make two different variables reference the exact same object. 

```java
public class Main {
    public static void main(String[] args){
        Person doug = new Person();
        Person liz = doug;

		System.out.println(doug);
		System.out.println(liz);
    }
}
```

This outputs:

> Person@511d50c0
> Person@511d50c0

In this case, the hash code is the same because both variables reference the same instance of the Person object. 

Imagine a person holding an apple. Now, imagine a _different_ person holding another apple.

* How many people are there? Two.
* How many apples are there? Two. 

Now imagine those same two people. They are both holding onto the same apple. (Perhaps they're fighting over it?!)

* How many people are there? Two.
* How many apples are there? One. 

Multiple variables can _point_ to the same object instance.

## Properties

**Syntax:** `<access modifier> <variable definition>`

Properties are variables that belong to a class. This is the data that defines your object. Properties are defined within the curly braces that define a class' body. Typically these are added immediately after the opening curly brace at the very top of the class' body. You can define as many properties as you wish, but they must all have different names.

One property that all real people have is a name. So, let's make our programatic model of a person have a name.

```java
public class Person {
    // this is the person's name
    public String name = "";
}
```

This code adds a single `String` property named `name` to the `Person` class. Because we set the access modifier to public, any other code can get or set the name of Person objects.

```java
public class Main {
    public static void main(String[] args){
        Person doug = new Person();
        doug.name = "Doug";

        Person liz = new Person();
        liz.name = "Liz";

        System.out.println(doug.name);
        System.out.println(liz.name);
    }

}
```

In this example we're again creating two different instances of the `People` class and assigning them to the variables `doug` and `liz`. We then set the `name` property for that instance, which is the property we just defined. Take particular note of the `.` "dot" character. This dot tells Java to get the value of the `name` property from the specific `Person` instance in the variable `doug`.

A person is not defined by a single property. I am not just my name. So, let's add a few more properties to our Person class. I've also added some comments to help explain what the code.

```java
/**
 * The Person class represents a person.
 */
public class Person {
    /**
     * The person's name.
     */
    public String name = "";

    /**
     * The person's age
     */
    public int age = 0;

    /**
     * The person's height
     */
    public double height = 0;   
}
```

Now we have more properties we can use.

```java
public class Main {
    public static void main(String[] args){

        // create a Person for Doug
        Person doug = new Person();
        doug.name = "Doug";
        doug.age = 38;
        doug.height = 6.0;

        // create a Person for Liz
        Person liz = new Person();
        liz.name = "Liz";
        liz.age = 38;
        liz.height = 5.5;

        // Print details to the console
        System.out.println(doug.name + " is " + doug.age + " years old and " + doug.height + " feet tall.");
        System.out.println(liz.name + " is " + liz.age + " years old and " + liz.height + " feet tall.");
    }

}
```

This code should be fairly clear. As before, we're creating two Person objects and setting their properties. Also, outputting more information about each Person instances to the console than previously.

## State

Properties are used to hold an object's _state_. State is the exact set of values that we are using to describe an object at any point in time. 

```java
// create a Person for Doug
Person doug = new Person();
```

As soon as I instantiate a new Person object it has state. The state is that the person has no name, is 0 years old, and is 0 feet tall. This is the default state. 

However, when I set an object's properties, I change its state. 

```java
doug.name = "Doug";
doug.age = 38;
doug.height = 6.0;
```

This code updates the Person's state. Now the person is named Doug, is 38, and 6 feet tall. An object's state stays constant until changed by code.

## Constructors

**Syntax:** 

```java
<access modifier> <Class name>(<constructor arguments){
	<body of constructor>
}
```

Constructors are defined within the curly braces that denote a class' body. Typically constructors are placed after class properties. 

Constructors are used to define the initial state of a new object. For our Person class, the default state is that a person has no name, is 0 years old, and is 0 feet tall. This isn't a very good model of reality. Let's add a constructor to resolve this:

```java 
/**
 * The Person class represents a person.
 */
public class Person {
    /**
     * The person's name
     */
    public String name = "";

    /**
     * The person's age
     */
    public int age = 0;

    /**
     * The person's height
     */
    public double height = 0;

    /**
     * Create a Person and set the default values;
     * @param name The person's name
     * @param age The person's age
     * @param height The person's height
     */
    public Person(String name, int age, double height){
        this.name = name;
        this.age = age;
        this.height = height;
    }

}
```

Let's look only at the Person constructor:

```java
public Person(String name, int age, double height){
	this.name = name;
	this.age = age;
	this.height = height;
}
```

In this example the access modifier is `public`. This means that any code can call the constructor when instantiating a new `Person` object. 

The next word in the constructor is "`Person`", which must match the class name. This is how Java knows that this chunk of code is a constructor. 

What follows next are a the constructor's _arguments_. An argument is a variable passed into a block of code when it's invoked. This constructor takes three arguments when a Person is instantiated, all of which must be provided. These are `name`, `age`, and `height`, which are respectively `String`, `int` and `double` variables. We can use these variables inside the body of the constructor.

Everything between the curly braces is the body of the constructor. In this example the constructor body is:

```java
this.name = name;
this.age = age;
this.height = height;
```

The body of the constructor introduces a new keyword, `this`. The `this` keyword is a reference to the current instance of an object. The `doug` variable we've been working with is an instance of the `Person` class. That instance has it's own state that is distinct from the state of the `liz` instance. The `doug` instance's `this` scope refers only to the properties on the `doug` instance. The `liz` instance's `this` scope refers only to the properties on the `liz` instance.

So, `this.name = name` sets the current instance's `name` property to be the value passed into the `name` argument. 

Now, when we create a new instance of a `Person` class we must provide three constructor arguments, `name`, `age`, and `height`. Here's how we'd do that:

```java
public class Main {
    public static void main(String[] args){

        // create a Person for Doug
        Person doug = new Person("Doug", 38, 6.0);

        // create a Person for Liz
        Person liz = new Person("Liz", 38, 5.5);

        // Print details to the console
        System.out.println(doug.name + " is " + doug.age + " years old and " + doug.height + " feet tall.");
        System.out.println(liz.name + " is " + liz.age + " years old and " + liz.height + " feet tall.");
    }

}
```

Adding the constructor has enforced our requirement that new instances of `People` be given a name, age, and height. We can still modify these properties after the object is constructed.

## Methods

**Syntax:**

```java
<access modifier> <return type> <method name>(<method arguments>){
	<method body>
}
```

There are two defining characteristics of a programatic object:

* It holds its own data
* It has methods that can interact with that data

So far our Person class only holds data, but it doesn't do anything with that data. It's not uncommon to write a class that only holds data. For that matter, you might reasonably have a class that has methods, but no data. Because we are trying to model the real world with our Person class, we should imbue it some behaviors.

You give classes the ability to "do stuff" (not a technical term) using methods. A _method_ is a chunk of code in a class that, well, _does stuff_. For example, it could perform a calculation, store data in properties, write a file to disk, or anything else.

Methods are defined anywhere within the curly braces that define a class' body. Typically these are added after constructors. You can have as many methods as you wish. By convention, method names start with a lower case letter just like variable names. Method names should express what the method does. 

Real people in the physical world give high fives to each other. Let's model that in our `Person` class. Let's declare that a Person can receive high five.

```java
/**
 * The Person class represents a person.
 */
public class Person {
    /**
     * The Person's name
     */
    public String name = "";

    /**
     * The Person's age
     */
    public int age = 0;

    /**
     * The Person's height
     */
    public double height = 0;

    /**
     * Used to count how many high fives this Person has received.
     */
    private int highFivesReceived = 0;

    /**
     * Create a Person and set the default values;
     * @param name The person's name
     * @param age The person's age
     * @param height The person's height
     */
    public Person(String name, int age, double height){
        this.name = name;
        this.age = age;
        this.height = height;
    }

    /**
     * Allows a person to receive a high five.
     */
    public void receiveHighFive(){
        this.highFivesReceived++;
    }

}
```

This code has two significant updates. Firstly, we added a new property:

```java
private int highFivesReceived = 0;
```

This is similar to the other properties we already had. The difference is that the access modifier has been set to `private`. The `private` access modifier tells Java that no code other than the Person class itself can set or update the highFivesReceived property. 

**Remember:** Only you can touch your privates.

<!-- todo: demo this in class -->

The other significant bit is the `receiveHighFive()` method itself:

```java
public void receiveHighFive(){
	this.highFivesReceived++;
}
```

This method has a `public` access modifier. This means that any code can invoke this method. The `void` keyword means that this function doesn't return anything to us when we invoke it. The name of the method is `receiveHighFive`. Because the parenthesis are empty, the method doesn't accept any arguments. This means we can't provide any data when the method is invoked. Finally, the body of the method is `this.highFivesReceived++`, which increments the Person class' `highFivesReceived` property.

We can invoke this method as follows:

```java
public class Main {
    public static void main(String[] args){

        // create a Person for Doug
        Person doug = new Person("Doug", 38, 6.0);
        doug.receiveHighFive();

        // create a Person for Liz
        Person liz = new Person("Liz", 38, 5.5);

        // Print details to the console
        System.out.println(doug.name + " is " + doug.age + " years old and " + doug.height + " feet tall.");
        System.out.println(liz.name + " is " + liz.age + " years old and " + liz.height + " feet tall.");
    }

}
```

This shows the `receiveHighFive()` method being invoked on the `doug` instance of the `Person` class. However, when we run this code we can't tell that anything has changed at all. There's really no way we can use this fact in our program yet. We can't simply update our `System.out.println()` expression in the `Main` class. This is because the `Main` class can't access the `Person` class' private `highFivesReceived` property.

This presents us with a bit of a conundrum. If we make the `highFivesReceived` property public, a rouge programmer could easily set this to any value they want. But, if we keep the property private, only the Person itself knows. If only there were an elegant solution to this problem...

## Accessors and Mutators

Accessors and Mutators, colloquially (and acceptably) known as Getters and Setters are simply methods that are used to read and write private properties. In the case of our `Person` class we could add a "getter" that returns the number of high fives a `Person` object has received. 

```java
/**
 * The Person class represents a person.
 */
public class Person {
    /**
     * The Person's name
     */
    public String name = "";

    /**
     * The Person's age
     */
    public int age = 0;

    /**
     * The Person's height
     */
    public double height = 0;

    /**
     * Used to count how many high fives this Person has received.
     */
    private int highFivesReceived = 0;

    /**
     * Create a Person and set the default values;
     * @param name The person's name
     * @param age The person's age
     * @param height The person's height
     */
    public Person(String name, int age, double height){
        this.name = name;
        this.age = age;
        this.height = height;
    }

    /**
     * Allows a person to receive a high five.
     */
    public void receiveHighFive(){
        this.highFivesReceived++;
    }

    /**
     * Gets the number of high fives this Person has received.
     * @return The number of high fives
     */
    public int getHighFivesReceived(){
        return this.highFivesReceived;
    }

}
```

This update to the Person class adds a new method, `getHighFivesReceived()`. Just like the `receiveHighFive()` method, this new method is public and accepts no arguments. But, unlike the `receiveHighFive()` method, this new method returns a value. This is denoted by the `int` keyword after the access modifier and before the method name. This tells Java that any invocations of this method will produce an integer value. 

In the same way that the `+` addition operator returns the sum of two values, invocations of the `getHighFivesReceived()`  will return the number of high fives a particular `Person` object has received.

I'll now update the `Main` class so that we can show how many high fives the `Person` has received.

```java
public class Main {
    public static void main(String[] args){

        // create a Person for Doug
        Person doug = new Person("Doug", 38, 6.0);
        doug.receiveHighFive();

        // create a Person for Liz
        Person liz = new Person("Liz", 38, 5.5);

        // Print details to the console
        System.out.println(doug.name + " is " + doug.age + " years old and " + doug.height + " feet tall. This person has received " + doug.getHighFivesReceived() + " high fives.");
        System.out.println(liz.name + " is " + liz.age + " years old and " + liz.height + " feet tall. This person has received " + liz.getHighFivesReceived() + " high fives.");
    }
    
}
```

This results in the following output:

> Doug is 38 years old and 6.0 feet tall. This person has received 1 high fives.
> Liz is 38 years old and 5.5 feet tall. This person has received 0 high fives.

## Responsibilities 

I like to think of classes as having _responsibilities_. I am responsible for writing this document and making it understandable. You are responsible for reading it and learning the material. The Person class is responsible for all things Person-y in our program.

It doesn't make sense for multiple bits of code to do the same thing. As an example, let's think about the description of the `Person` objects the `Main` class is outputting. 

What if I wrote some other class that also interacts with the `Person` class? What if that other class also needs a description of a `Person` object? Do I copy and paste the code from the `Main` class? What if the description needs to be changed at some point? 

I don't think the `Main` class (or any other class) should have the responsibility to describe a `Person` class. The `Person` class should be solely responsible for that. Furthermore, the Main class is already doing a lousy job of it as it doesn't take into account plurality. For example, "This person has received 1 high fives."

To facilitate this, we could add a method to the `Person` class that returns a description of a `Person` object.

```java
/**
 * The Person class represents a person.
 */
public class Person {
    /**
     * The Person's name
     */
    public String name = "";

    /**
     * The Person's age
     */
    public int age = 0;

    /**
     * The Person's height
     */
    public double height = 0;

    /**
     * Used to count how many high fives this Person has received.
     */
    private int highFivesReceived = 0;

    /**
     * Create a Person and set the default values;
     * @param name The person's name
     * @param age The person's age
     * @param height The person's height
     */
    public Person(String name, int age, double height){
        this.name = name;
        this.age = age;
        this.height = height;
    }

    /**
     * Allows a person to receive a high five.
     */
    public void receiveHighFive(){
        this.highFivesReceived++;
    }

    /**
     * Gets the number of high fives this Person has received.
     * @return The number of high fives
     */
    public int getHighFivesReceived(){
        return this.highFivesReceived;
    }
    
	/**
     * I return a description of the Person
     * @return The Person's description
     */
    public String describe(){
        String years = this.age == 1 ? "year" : "years";
        String feet = this.height == 1 ? "foot" : "feet";
        String fives = this.getHighFivesReceived() == 1 ? "five" : "fives";

        return this.name + " is " +
                this.age + " " + years + " old and " +
                this.height + " " + feet + " tall. " +
                this.name + " has received " +
                this.getHighFivesReceived() + " high " + fives + ".";
	}
}
```

In here you can see that I've added another public method, `describe()`. The `describe()` method returns a description of the person. Now I can use this function anywhere I want to get a description of the person.

On a side note, these three lines each use the [ternary operator](https://en.wikipedia.org/wiki/%3F:):

```java
String years = this.age == 1 ? "year" : "years";
String feet = this.height == 1 ? "foot" : "feet";
String fives = this.getHighFivesReceived() == 1 ? "five" : "fives";
```

The ternary operator is similar to an if conditional, but otherwise unique to its own syntax. You can read the first line like this:

> If `this.age` is 1, then return "year". Otherwise return "years".

The other lines are the same.

```java
public class Main {
    
    public static void main(String[] args){

        // create a Person for Doug
        Person doug = new Person("Doug", 38, 6.0);
        doug.receiveHighFive();

        // create a Person for Liz
        Person liz = new Person("Liz", 38, 5.5);

        // Print details to the console
        System.out.println(doug.describe());
      	System.out.println(liz.describe());
    }
    
}
```

In this code I'm now invoking the describe() method on the Person objects instead of writing out my own ugly version. Rather than having four copies of the same ugly chunk of code I now have one ugly chunk of code in a logical place that I invoke four times. As a result, the Person class has responsibility for describing itself and the Main class is significantly cleaner and easy to read. 

<!-- exercise: model a playing card and a deck of cards -->

# Wrap Up

That ends the Java Crash Course. Hopefully you've learned enough that you feel like you've been pointed in the right direction. Keep going!

Here are some suggestions:

* Read [a book on Java](http://www.amazon.com/Test-Preparation-Books/b?node=3608&ref=spkl_6_1_2269486622&qid=1458932827&pf_rd_p=2269486622&pf_rd_m=ATVPDKIKX0DER&pf_rd_t=301&pf_rd_s=desktop-auto-sparkle&pf_rd_r=0WS4Y05B4EBY8GRWSNVD&pf_rd_i=java)
* Work through the [Codecademy course on Java](https://www.codecademy.com/learn/learn-java)
* Do the [Java exercises on Codewars](http://www.codewars.com/?language=java)
* Attend [Java meetups](http://www.meetup.com/Triangle-Java-Users-Group/)

And, of course, take my [Java class here at The Iron Yard](https://www.theironyard.com/courses/java-and-clojure.html)!