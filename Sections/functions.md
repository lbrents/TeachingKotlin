# Functions

Let's go back to the very first section of this guide, the program entry point. Before, we kinda glossed over it, but our program entry point was something like...

``` kotlin
fun main() {
    // Code goes here...
}
```

This code right here is actually called a function. Our main function to be specific. Kotlin looks for a function with the name of 'main' as the starting point of our code. Without it, Kotlin does not know what to do and will most likely give a lot of errors.

So what is a function? The answer in programming is that it is a reusable chunk of code that we can reference later for our convenience. Let's look at an example with a template as well.

``` kotlin
// Function template...
// fun [function name]() {
//      [your code here]
// }

// Create a function called 'saySomething'
fun saySomething() {
    println("Hello, world!")
}

fun main() {
    // Use, or 'call', our saySomething function...
    // It will print "Hello, world!" to the console.
    saySomething()
    // And if we want to, we can repeat this as many time as we want...
    saySomething()
    saySomething()
    saySomething()
    saySomething()
}
```

First, we use the `fun` keyword to start declaring our function. Then we give it a name, in this case it was `saySomething`. After that we put some parentheses after the name, but for now let's just know that they always go right after the name. And finally, we put our code in the curly brackets right after.

Those are the basics of creating the least interesting type of function, one that does the same thing **every** time. What if we wanted our function to do something different under different circumstances?

This is the part where I introduce the concept of inputs and outputs. This part if fairly intuitive (probably). Based on some set of input, we can perform some calculations on those input to produce an output. When those inputs change, our output can change with it.

That's a lot of words and not a lot of things happening, so how about an example?

``` kotlin
// Function with arguments template...
// fun [function name]( [arg name]: [arg type], [more arguments if needed], ... ) {
//     [code goes here]
// }

fun areaOfASquare(x: Double, y: Double) {
    println(x * y)
}

fun main() {
    // The length and width of a table or something in inches...
    var length: Double = 48.4
    var width: Double = 61.8
    // If we wanted the area of that table, we could use our function
    var area = areaOfASquare(length, width)
    println(area)
}
```

In our example, we declared another function called `areaOfASquare`. However, you might have noticed that we actually have stuff inside of our parentheses this time. It turns out, those parentheses are where we put our function's inputs or otherwise known as function arguments.

The way to do this is to give each input a name, and then a type. And if want multiple inputs then we seperate them by commas.

When we call a function with inputs, there are two ways we can specify our inputs. The following is going to be an example of both methods.

``` kotlin
// Calling a function with inputs requires us to specify our inputs in order,
//  so x goes first, and then y.
areaOfASquare(10, 20)

// If we want to be more specific, then we can choose to specify our inputs by name
//  instead. This does not require our inputs to be in order.
areaOfASquare(x = 40, y = 6)
```

Another cool thing about the inputs of a function is that sometimes you don't even need to specify all of them. If we have a function with an argument, we can actually set a default value for that argument. Let's take a look at how that works.

``` kotlin
// Function to say hello to someone...
fun greeting(name: str = "Ishmael") {
    println("Hello, " + name + "!")
}

// Let's greet both Heathcliff and Ishmael
greeting("Heathcliff")
greeting() // Does not need anything because the default is specified!
```

The last thing about basic functions is the output side, but what does that mean in terms of programming? Simply put, it means if we define a function with an output then it will always yield some value of the output's data type. Once again, that's a lot of words and not a lot of code, so here's an example.

``` kotlin
// Template of a function with inputs and an output...
// fun [function name]( [inputs] ): [data type of output] {
//     [code goes here]
// }

// Rewriting our area function to return the area instead of printing it...
fun areaOfASquare(x: Double, y: Double): Double {
    return x * y
}

// Testing out our better function...
val area = areaOfASquare(10, 7)
println("The calculated area is:")
println(area)
```

In the example, we have two different things going on. First, we now have an extra bit at the end of our function declaration right after the inputs. This the data type of the output that we want our function to have.

Second, there is a new keyword we are using. The `return` keyword is exclusively used at the end of a function to output, or **return**, a value. Combined with some inputs, the value of the output can be anything you want, which is what makes functions so useful.

___

[Lambda Functions](lambdas.md)
