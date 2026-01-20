# The Program Entry Point

Let's start by asking the question: What code do we start with?

This answer is relatively simple for a programming language. Copy and paste the following code into the editor and click the "Run" button. After you do that, let's go over what this code does.

``` kotlin
fun main() {
    println("Hello, world!")
}
```

First things first, lets ignore this line in the middle `println("Hello, world")` and explain what all the fluff surrounding it is.

The code `fun main()` is what is called our program's entry point. It is where the computer is told to start executing our code. The curly brackets `{ }` following are the markers telling the computer where the code for our program's entry point is.

For now, we don't have to know exactly what all that means. The key takeaway is that whenever we want to write code in Kotlin, it must be inside those curly brackets following the `fun main()`.

Next, let's take a look at the line `println("Hello, world!")`.

The `println` part of this line is the name of a function called the "print line" function. All the stuff inside the following parentheses are known as that function's parameters. Simply put, the print line function takes its parameters and prints them to the console when it is executed. That is why when we run our program, we can see a console pop up with the text "Hello, world!".

![Function Basics](../Images/HW_01.png)

> [!NOTE]
> When we use a function, we say we are "calling" that function. So in this case, we can say that we are calling the `println` function.

___

[Printing To The Console](printing.md)
