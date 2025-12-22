# Cheatsheet

## Program Entry Point

``` kotlin
fun main() {
    // Put code here
}
```

## Printing

``` kotlin
// Printing strings
println("Strings go in quotes")

// Printing numbers
println(1 + 1) // = 2
println(-4 * 4) // = -16
```

## Datatypes

| Type | Description |
| ---- | ----------- |
| Int  | An Int (integer) is what we refer to as whole numbers. It represents all numbers between infinity and negative infinity, but no numbers with decimal points like 2.2 or -10.07. |
| Double | A Double is what we refer to as a decimal number. It theoretically represents all numbers between infinity and negative infinity as well as numbers like 2.2 and -10.7. Behind the scenes, doubles can be quite complicated so just know that ideally, we should only be using these when we need the precision. |
| Boolean | A Boolean represents the values of true and false. We use these to represent states like being either on or off. There are also some calculations we can perform, specific to booleans, that make them very useful.
| String | A String is just a string of text. Kotlin only knows if text is actually a string if it is surrounded by double quotes. |

## Variables

``` kotlin
// Variable template:
// var [name]: [datatype] = [data]

// Variables can be edited
var myVariable: Int = 10    // 10
myVariable = 20             // 20
myVariable = myVariable + 5 // 25

// Values are always constant
val myValue: String = "This too shall pass"
myValue = "Something else..." // This will cause an error

// Array template
// var [name]: Array<[datatype]> = arrayOf([data])

var myArray: Array<Int> = arrayOf(1, 2, 3, 4, 5)
myArray[0] // is the 0th index with the value 1
myArray[1] // is the 1st index with the value 2
myArray[2] = 14 // Changes the 2nd index to the value 14
```

## Conditionals

``` kotlin
// Equality operators
2 == 4 // -> False // Equals
2 != 4 // -> True  // Does not equal
1 >  4 // -> False // Greater than
1 <  4 // -> True  // Less than
3 >= 3 // -> True  // Greater than or equal to
3 <= 6 // -> True  // Less than or equal to

// Boolean logic
true  && true  // -> True  // Logical AND
true  && false // -> False 
true  || true  // -> True  // Logical OR
false || false // -> False
!true          // -> False // Logical NOT
!false         // -> True

// If statement template
// if ( [boolean] ) { [code here] }

// If
if (5 > 4) {
    println("5 is greater than 4!")
}

// If-Else
if (4 > 5) {
    println("4 is greater than 5?")
} else {
    println("4 is NOT greater than 5!")
}

// If-Else If-Else
if (2 == 0) {
    println("2 is equal to 0?")
} else if (2 == 1) {
    println("2 is equal to 1?")
} else if (2 == 2) {
    println("2 is equal to 2!")
} else {
    println("2 is not equal to 2?")
}
```

## Loops

``` kotlin
// For loop template
// for ([name] in [array]) {
//     // Do something with [name]
// }

var myNames: Array<String> = arrayOf(
    "Gregor", "Rodion", "Sinclair", "Yi Sang",
    "Ishmael", "Heathcliff", "Don Quixote", "Hong Lu",
    "Ryoshu", "Meursault", "Outis", "Faust"
)
for (name in myNames) {
    println(name + " is the best!")
}

// Iterating over a range with a for loop
for (x in 1..100) {
    println(x)
}

// While loop template
// while ( [condition] ) {
//     // Executes if true
// }

var index: Int = 10
while (index > 0) {
    println(index)
    index -= 1
}

// Using breaks and continues
val myFavorite: String = "Don Quixote"
for (name in myNames) {
    if (name == myFavorite) {
        break // break out of the loop
    } else {
        continue // continue to the next iteration
    }
}
```
## Functions

``` kotlin
// Function template
// fun [name]( [arguments] ): [Return type] {
//     // Code here
//     return [data of same return type]
// }

// No arguments, no return
fun doSomething() {
    println("Bon voyage, your mermaid's setting sail")
}

// Multiple arguments, no return
fun doAnotherThing(x: Double, y: Double, thing: Str) {
    println(thing)
    println(x + y)
}

// Multiple arguments, returns a value
fun addNumbersTogether(a: Double, b: Double, c: Double) -> Double {
    return a + b + c
}

// Arguments with default values
fun defaultSomething(name: String = "Gregor") {
    println("His name is " + name)
}

// Calling these functions
doSomething()
doAnotherThing(1.2, 55.3, "Ishmael")
var sum: Float = addNumbersTogether(1.1, 2.2, 3.3)
defaultSomething() // prints "His name is Gregor"
defaultSomething("Sinclair") // prints "His name is Sinclair"

// You can explicity state which value goes to which argument by their names
sum = addNumbersTogether(
    b = 19.0
    a = 73.9
    c = -42.2
)
```
### Lambda Functions

``` kotlin
// Functions can also be treated like variables
val addLambda: (Double, Double, Double) -> Double = addNumbersTogether
val result = addLambda(10.0, 20.0, 30.0)

// Because functions can be like variables, we can use them as arguments for other functions
fun myAlgorithm(operation: (Int, Int) -> Int): Int {
    return operation(4, 5) * 2
}

// You can use an already defines function when calling this
fun adder(a: Int, b: Int): Int {
    return a + b
}
val someNumber: Int = myAlgorithm(adder)

// Or you can create one when you need it for that specific function call
val otherNumber: Int = myAlgorithm(
    operation = { x: Int, y: Int ->
        x * y // returns the multiple of the two arguments
    }
)
```

## Null Values

``` kotlin
// Adding a question mark to the type of a variable makes it nullable
var myName: String? = "Faust"
// When a variable is nullable, we can assign to it the value 'null'
myName = null
// This can mean many things, for example in this case it could mean we don't know what my name is.

// When a variable is nullable, we MUST make sure we safely handle its value to make sure we do not accidentally use it as it's type when it is null.
var myInt: Int? = null
myInt = myInt + 10 // This is an error because you cannot add 10 to a null value

// We can use a shortened version of an if-else statement to handle nullable variables.
// This is called the elvis operator
val notNullableInt: Int = myInt ?: -1 // -1 if myInt is null
```

## Composables

The following link contains a list of commonly used ui components that we can make.
https://m3.material.io/components

Each component is a function that is called wherever you want to display it.

Components are placed inside layouts.

## State

Ui state is stored in mutableStateOf variables.


