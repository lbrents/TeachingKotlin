# Loops

Alright, so let me ask this question now... What if we wanted to do something very repetitive, like loop the same code over and over until a condition is met? To do something like that, we can use what is called a `while` loop. Let's look at an example to get an idea of what I am talking about.

``` kotlin
var myNumber: Int = 0

// Let's loop until my number is 100 or something
// This checks if myNumber is less than 100,
// and if it is then the loop continues.
// If at any point, this condition is false, then
// the loop stops.
while (myNumber < 100) {
    // Here is the code that gets repeated for every loop
    // I am going to increment the number so eventually it will be greater than 100
    myNumber = myNumber + 1
    // Let's also print the value of myNumber to see this in action
    println(myNumber)
}

println("Done!")
```

Copy this code into your main function and then run it to see the loop in action.

So far, this is one type of loop: A loop that keeps going until a condition becomes false. In programming, there is another type of loop called a for loop. The purpose of this one  in Kotlin is not to loop until a condition is met, but to instead loop through a collection of something. Our previous example had us looping until our variable `myNumber` went from 0 to 100, but with a for loop we can actually simplify this process.

``` kotlin
// Loop through the numbers 0 to 99
// The last number is exlusive so it stops at the number before
for (i in 0..100) {
    println(i)
}
```

Let's go over what's going on here. First, inside the parenthesis we do not have a conditional like we have seen before. Instead this is a different syntax that declares the name of a variable, in this case `i`, that will represent every number in the loop.

The `0..100` is what we call a range. In short, this is actually data type just like how numbers and strings are data types, but these are used almost exlusively in for loops. The first number is your starting point, and the last number is the stopping point. Just make sure to remember that the range stops at the number before, 99 in this case.

Inside the for loop, we can use our variable `i` just like we normally would with the exception being that we cannot change it's value because the for loop does this for us.

That's cool and all, but is that it? The answer is (unfortunately) no. For loops are intended to loop through collections of things. So now is probably a good time to bring up the fact that in programming, we can actually create collections of variables. Kinda.

Let me ask this: What if we wanted to create a bunch of variables? Like, a lot of variables? We can do just that with something called an array.

An array is something that stores multiple values of the same data type all in one place, so if we wanted to create 100 variables to store some numbers then we can use an array to simplify that.

``` kotlin
var arrayOfNumbers: Array<Int> = arrayof(1, 5, 9, 10, -27)
```

First, this code creates a variable of the array data type. This is different from all of the other data types because on it's own, it does not mean very much. It actually needs another data type so that Kotlin knows what we want to put *inside* of our array. In the example, we did this by putting the data type we want in the array inside of angle brackets after the `Array` data type.

Hopefully that makes sense so far. If not, thats ok. It's like 4AM right now because I got busy doing other stuff instead of writing this.

Here is an example of using a for loop to iterate over an array of values.

``` kotlin
// All of the names we want to do stuff with...
var names: Array<String> = arrayOf(
    "Gregor", "Rodion", "Sinclair", "Yi Sang",
    "Ishmael", "Heathcliff", "Don Quixote", "Hong Lu",
    "Ryoshu", "Meursault", "Outis", "Faust"
)

// Using a for loop to do stuff with these names...
for (name in names) {
    println(name + " is cool!")
}
```

For now, that's the basic of loops. I'll update this later to make things more coherent and add some exercises as well.

___

[Functions](functions.md)
