# Printing

In our first program, we call the `println` function. This is actually one of the most important functions to learn about when starting to code. This is because it is one of the easiest ways to help debug your code. So let's learn about how we can use this function.

We first printed some text to the console. To print plain text, we have to make sure that the text we are printing is inside double quotes `""`. Otherwise the computer will think we are trying to print something else and might break.

Right under our "Hello, world!" line, call the `println` function again and make it print a message of your choice.

Printing text is cool and all, but we can actually do a lot more than that. For example, Kotlin lets us perform mathematical calculations very easily. Replace the code inside your main function with the following code and then run it to see how this works.

``` kotlin
println(1 + 1)
println(10 - 15)
println(-2 * 8)
println(10 / 2)
```

So if we make our parameter some math instead of a message inside double quotes, we can print their results to the console. Kind of like a calculator.

The main takeaway here is that if we want to print a message, we surround our message in double quotes `""` and if we want to print some math, we just type out our math like it's a calculator.

But why is any of this important?

Simply put, we use the `println` function to test our code. When our code starts to get complicated and messy (it will), we may not know the value of certain things. This is where we can use the `println` function to see what that value is and make sure that everything is working as intended.

The last thing I would like to cover, before moving on to the more fun stuff, is putting comments in our code.

Before we even get to the point of having to print stuff to the console to understand what is going on in our code, we can write comments to document how our code works and make it easier to read.

So how do we put comments in our code? The answer is with double slashes `//`. In our code, everything past a pair of forward slashes will be considered a comment until the next line. If we want to write a comment that is going to span more a single line, we can instead use a forward slash followed by an asterisk `/*` to start a multi-line comment. To end a multi-line comment, we type an asterisk followed by a forward slash `*/`.

You don't have to copy and paste this code, but reading it is a good idea.

``` kotlin
/* This is a multi-line comment,
    everything in here is not going to be counted as code.
    Even if I write
    println("Hello, world!")
    it will not run.
*/

// This is a single line comment.

println(3.1415 * 2) // This will always be 2 pi.
```

___

[Data Types](data_types.md)
