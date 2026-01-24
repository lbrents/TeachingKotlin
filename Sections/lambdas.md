# Lambda Functions

This is probably the most complicated part of this guide, so it's definitely fine if this doesn't make sense at first. The key takeaway is going to be recognizing **when** you need a lambda function, not the complicated stuff about what exactly they are.

So after that preface, what exactly is a lambda function? A lambda function is essentially a function that can be treated like a variable. It differs in how you make it and even has a data type. But if we can already create functions normally, then why would we need another way just so we can put them into variables?

The answer is so that we can make functions with lambda functions as arguments. I'm getting ahead of myself though, so lets look at how to create a lambda function.

``` kotlin
// Creating a variable that is a lambda function
var myLambda = { println("Hello, world!") }

// We can call this lambda like a function normally would...
myLambda() // Prints "Hello, world!"
```

Now we have a lambda function stored in a variable, but what is it's data type? To determine that, let's look at the function's inputs and outputs.

In this case, `myLambda` has no inputs and no outputs, so it's data type would be this: `() -> Unit`. Ok, we've seen data types like `Int` and `String` before, but this one is pretty different. Fortunately, it does make sense.

The parentheses are the function's input argument data types. So if we had a lambda function that took two integer arguments and had no output, the data type would change to `(Int, Int) -> Unit`. If we wanted to have just one string argument insteadm, it would become `(String) -> Unit`

For the output section, our examples currently show us using this `Unit` thing. I'm too lazy to look up what that actually is, so just know that we put `Unit` there when we do not have an output.

But what if we do want an output? The answer is simple. Suppose we want a lambda function with one integer argument and an integer output. The data type would change to `(Int) -> Int`. If we want two integer inputs and a boolean output, the data type would be `(Int, Int) -> Boolean`.

Hopefully this makes sense so far because the next part is a bit more complicated.

How exactly do we use the inputs for a lambda function? You might have noticed that we don't actually given them names. Usually, we define the names of our arguments inside the parentheses after the function name, but for lambda functions we actually give our inputs names right before the code. Here is how that works.

``` kotlin
// Function to add two doubles together and then divide by 3
// a is the name of the first double and b is the name of the second
// The arrow at the end seperates the naming of the inputs with the
//  actual code
var myCalculation: (Double, Double) -> Double { a, b ->
    (a + b) / 3
}
```

It's kind of a weird way to do it, but I promise that there is a reason it is done this way.

Another thing you might have noticed is that we don't actually use the `return` keyword like we do in normal functions. I'm going to be honest here, I think it's dumb that we don't, but I'm sure the creators of Kotlin had some sort of reason for this. But anyways... How do we return then? 

The rule for returning from a lambda function is that the last value in the lambda function code is what is returned. In our example above, we only have one line, so let's look at another example that spreads it out a bit.

``` kotlin
// Same function, just with more code this time...
var myCalculation: (Double, Double) -> Double { a, b ->
    val multiplied: Double = a * b
    multiplied = multiplied / 3
    multiplied // This is the last value of the function so it gets returned
}
```

So far, those are the basics of lambda functions, but what was the point of all of this? I already said the answer, but I'll say it again: Function arguments.

Because lambda functions have a data type, we can create functions that take functions as arguments. This actually let's us do a lot of cool stuff, but for now let's just look at how we can do this.

``` kotlin
// Creating a lambda for some calculation...
var calculation: (Double, Boolean) -> Double { number, state ->
    var result: Double = number
    if (state) {
        result = number * 2
    } else {
        result = number / 2
    }
    // Return result here
    result
}
```

``` kotlin
// Creating a function that takes a lambda...
fun customCalculation(length: Int, calc: (Double, Boolen) -> Double) {
    for (i in 0..length) {
        // Let's print the result of our lambda here
        result = calc()
    }
}
```



