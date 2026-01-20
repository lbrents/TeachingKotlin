# Conditionals

If you have some programming experience, if statements are what are known as conditionals. Put simply: If something is true, do something. It is called a conditional because it requires a condition to be true in order to do something.

In Kotlin, the most basic form of a conditional is what is called an if statement. The following code is a basic template and example.

``` kotlin
// If statement template
// if ( [some boolean variable or expression] ) { [your code here] }

var lights: Boolean = true

// If the light is on, print to the console
if (lights) {
    println("The lights are on!")
}
```

To add on to this new concept, what if we want to do something if a condition is true and do something else if the condition is false?

Let me introduce the if-else statement.

``` kotlin
var lights: Boolean = false

// If lights are on, do something, otherwise do something else
if (lights) {
    println("This should never run!")
} else {
    println("The lights are NOT on!")
}
```

Hopefully that makes sense so far, but let's add on to this concept one last time. What if we want to chain a whole bunch of conditionals together? Let me finally introduce the else-if part of an if statement.

``` kotlin
var myNumber: Int = 10

// Checking if myNumber is less than, equal to, or greater than 5
if (myNumber == 5) {
    println("My number is 5")
} else if (myNumber < 5) {
    println("My number is less than 5")
} else if (myNumber > 5) {
    println("My number is greater than 5")
} else {
    println("Uh oh... something went wrong!")
}
```

One thing to note is that it is totally possible for multiple conditions to be true. But when the first condition to be true is reached, the code for that conditional is run and then the whole statement is exited.

And with that whirlwind tour of conditionals, we can now check the value of variables and do whatever we want based on that value.

___

[Loops](loops.md)