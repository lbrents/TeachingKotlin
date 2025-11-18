# Printing

A.K.A. Lock in, samurai. We have code to burn. But really though we use this for testing code.


### Hello, World!

Typically, the first program one writes when learning a new coding language is called the "Hello, world!" program. If you haven't figured it out yet, it will display the sentence "Hello, world!" to the console when we run it.

Go ahead and copy the following code into your main file in Android Studio and click the green arrow that will appear to the left of the start of your code. (As a side note, once you have clicked that green button once, you should be able to click the green arrow button at the top of the editor from now on to run your code.)

``` kotlin
fun main() {
    println("Hello, world!")
}
```

So... How does this work? Let's try to answer this one step at a time.

Every program requires a starting point which we call our main function. In Kotlin, we make our main function by typing the `fun` keyword followed by `main()` and then a set of curly brackets like we can see in the example above. Inside the curly brackets goes the code that we want to run at the start of the program.

We don't have to worry about what exactly all of that means just yet. The main takeaway should be the `println` (print line) function that we are using to display our text. What this function does is take whatever text or numbers that are inside the parentheses, and show them in the console window.

It is a rule to put double quotes `""` around any text so that Kotlin knows it is text and not anything else. For numbers, we do not have to worry about that. The following code is an example of both, so go ahead and paste that into our main function and then run it.

``` kotlin
println("Bon voyage, your mermaid's setting sail.")
println(1 + 3)
println(10 / 2)
```

If everything went well, then we should be seeing a stupid quote alongside some numbers printed to the console. Kotlin can do math, which is why the second part of the example works. Feel free to play around with that and change the numbers and operators and see what you get. The sky is the limit (probably).


### Comments

Before we move on to something slightly more interesting, something to know before writing too much code is how to write comments. A comment is simply just some text you can use to document how your code works or even disable a certain section of code.

To write a comment, start with double slashes followed by whatever text you want to make your comment.

``` kotlin
// This is a comment. We always start a comment with double slashes in Kotlin.
println("Hello, world!")
// println("This will not show because it is a comment!)
```

And lastly, to write a comment that spans more than just one line, we start with a slash and then an asterisk `/*`. To end a multi-line comment, we write an asterisk and then a slash `*/`. Everything in between will be treated as a comment.

``` kotlin
fun main() {
    /* I guess this is a
        multi-line comment.
    */
    println("Something")
}
```

Anyways... on to [Variables](variables.md).


---

### Back To [Table Of Contents](../README.md)
