# Printing

### Hello, World!

So far, this is the code we have.

``` kotlin
fun main() {
    println("Hello, world!")
}
```

Let's first dissect this one step at a time.

For now, just know that `fun main()` is required by Kotlin to know exactly where to start your program. This is called our main function.

The curly brackets tell Kotlin that everything in between is going to be code for our main function.

The actual code that we are running is the line `println("Hello, world!")`. Breaking this line up even further, we have a function called `println` (print line) that takes everything inside it's parentheses and *prints* it to the console.

[!IMPORTANT]
Something to remember is that if you want to print text to the console, all the text you want to print **must** be inside double quotes.

So now we know that if we want to print a message to the console, we have to call our `println` function and put our message in double quotes inside the function's parentheses.

Let's change the message in our program to whatever your heart desires and then run the program.

But...

### Performing Calculations

What if we wanted to do something a little more interesting than just printing text? Luckily, Kotlin lets us easily perform mathematical calculations and just as easily print them to the console like text.

Copy and replace the current code inside our main function with the following code and then run the program.

``` kotlin
println(100)
println(77 + 33)
println(10 - 50)
println(1000 * 42)
println(10 / 3)
```

Kotlin will run each `println` function sequentially for us. You should also notice that Kotlin calculated the result of the math we put inside the function's parentheses. And it doesn't have to be just a calculation either. The first `println` is just the number 100 and that prints just fine as well.

Lastly, one other thing you might notice is that 10 / 3 is not 3, but 3.333... repeating. For now, don't worry about why this happens because the variables section will explain properly (hopefully).

The main takeaway is that Kotlin can do math. Feel free to change the numbers and the operators to get a feel for how this works.

### But Why?

Simply put, we use the `println` function to test our code. When our code starts to get complicated and messy (it will), we may not know the value of certain things. This is where we can use the `println` function to see what that value is.

The last thing I would like to cover before moving on to the more fun stuff, is putting comments in our code.

Before we even get to the point of having to print stuff to the console to understand what is going on in our code, we can write comments to document how our code works and make it easier to read.

So how do we put comments in our code? The answer is with double slashes `//`. In our code, everything past a pair of forward slashes will be considered a comment until the next line. If we want to write a comment that is going to span more than a couple lines, then we can use a forward slash followed by an asterisk `/*` to start a multi-line comment. To end a multi-line comment, we type an asterisk followed by a forward slash `*/`.

You don't have to copy and paste this code, but reading it is a good idea.

``` kotlin
/* This is a multi-line comment,
    everything in here is not going to be counted as code.
    Even if I write
    println("Hello, world!")
    it will not run.
*/

// This is a single line comment.

println(10 / 3) // This will always be 3 and NOT 3.333 repeating.
```

... And now, on to Variables.

<p align="right">
    <a href='Variables.md'>Variables</a>
</p>

___

<p align="center">
    <a href='../README.md'>Table Of Contents</a>
</p>