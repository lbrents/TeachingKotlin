# Variables

A variable in programming is kind of like a box that stores a value for you. In Kotlin, we specify the data type that the variable will hold, and then the value it will initially have. To create a variable, we use the `var` keyword to start. The following code is a template of how to create a variable.

``` kotlin
// To create a variable...
// var [variable name]: [data type] = [value to initialize the variable with]

// For example...
var myVariable: Int = 10

// Another example using another data type
var anotherOne: String = "This is a string!"

// Last example...
var lastExample: Boolean = false
```

Following the template, this code creates three different variables, but so far this does nothing. If we do want to do something with a variable, however, all we need to remember is it's name to access it.

``` kotlin
// Declaring a variable...
var moneyIHave: Int = 10

// Payday happens here...
moneyIHave = moneyIHave + 90

// Bought something stupid again...
moneyIHave = 10

// Using that variable to create another variable...
var moneyINeed: Int = moneyIHave * 10 // Multiply by 10

// Printing the content of moneyINeed to the console...
println(moneyINeed)
```

And lastly, what if there is a number or value that we want to remember, but we know is not going to change? Kotlin has an answer for this with something called a constant. It follows the exact same template as a variable, but instead of using the `var` keyword, we use the `val` keyword instead. This makes sure that when we create our constant, it will **not** be able to change anywhere in the code.

``` kotlin
// Example of creating a constant variable...
val pi: Double = 3.1415
val name: String = "Kong Qiu"
val serialNumber = "O-01-04(-W)"

// If we uncomment this, we get an error
// name = "Jia Qiu"
```

___

[Boolean Logic](boolean_logic.md)
