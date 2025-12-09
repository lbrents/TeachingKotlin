# Variables

### Data Types

To address the allegations, remember how we calculated 10 / 3 before and we got 3 instead of 3.33333... something or other? That is because numbers without decimals are automatically forced to be whole numbers. In Kotlin, division using whole numbers will always result in a whole number, always throwing away the decimal point by rounding down.

Go Ahead and print to the console the result of 10.0 / 3.0 and see that the result looks a little more accurate.

So now we know that math with whole numbers will give us a whole number and math with decimal numbers will give us decimal numbers. But one thing to take note of is that if you want to perform some calculation and mix whole numbers with decimal numbers, the result will always be another decimal number.

So why is there a difference between whole numbers and decimal numbers?

The answer to that can be quite complicated so to give a general answer, it is because Kotlin uses something called data types. Data is pretty much any number or text that is stored in our program, but in order to make dealing with data easier, we categorize it into different types.

The following is a table categorizing the main types of data we will be using.

| Type | Description |
| ---- | ----------- |
| Int  | An Int (integer) is what we refer to as whole numbers. It represents all numbers between infinity and negative infinity, but no numbers with decimal points like 2.2 or -10.07. |
| Double | A Double is what we refer to as a decimal number. It theoretically represents all numbers between infinity and negative infinity as well as numbers like 2.2 and -10.7. Behind the scenes, doubles can be quite complicated so just know that ideally, we should only be using these when we need the precision. |
| Boolean | A Boolean represents the values of true and false. We use these to represent states like being either on or off. There are also some calculations we can perform, specific to booleans, that make them very useful.
| String | A String is just a string of text. Kotlin only knows if text is actually a string if it is surrounded by double quotes. |

> [!NOTE]
> There are more types than what is listed here, but for now these are the most important ones that we will be getting familiar with.

### Variables

So we know we can do math and stuff... but what do we do when we want to save our calculations and reuse them later? The answer is by creating a variable. 

And what exactly is a variable? A variable in programming is something that we use to store our data in. Each variable you create will always have a specific data type and will be able to store any value that is the same data type. Copy and replace the code inside your main function with the following code.

``` kotlin
// This does nothing
3 + 7

// But this will save the result in a variable
var myCalculation: Int = 3 + 7

// And this uses our variable
println(myCalculation)
```

Let's run this code and then go over it line by line.

You could probably guess that the output was going to be the number 10, but how exactly did we get there?

The first line `3 + 10` simply does nothing. It calculates the number 10, but that number has nowhere to go and is just ignored.

The second line is where things get interesting. We use the `var` keyword to tell Kotlin that what comes next is going to be a variable. Then we specify its name as `myCalculation` but we can actually make it any name we want as long it starts with a letter. If you happen to name a variable wrong, don't worry, Android Studio will most likely tell you what to do.

After we gave our variable a name, next comes a colon followed by the type of the variable. At this point we have started the process of creating a variable, given it a name, and given it a type. Lastly, we store a value to our variable by using an equals `=` sign followed by the value itself.

And there we have it, a integer variable named `myCalculation` that stores the number 10. But wait~ there's more. What do we do when we want to change the value of our variable? Thankfully, that's the easiest part.

Add this code right under where you created your variable and above the print statement and then run it.

``` kotlin
// Changing the value of myCalculation to something better
myCalculation = 200
```

Hopefully, if you did it right, the number printed to the console is now 200 instead of 10. That's right, once a variable is created, all we have to do to change it is type its name followed by an equals `=` sign followed by the new value.

Now let's use what we have learned so far. Copy and replace all your code inside the main function so far with the following code and then replace each `...` with the code it tells you to write.

``` kotlin
println("Enter a number:")
// This will read what you type into the console
// And store it into a variable.
// Don't worry about knowing how exactly this works.
var yourInput: Int = readln().toInt()

// (1)
// Create an integer variable here named 'favoriteNumber'
// and assign it the value of 'yourInput' * 10
...

// (2)
// Print the value of 'favoriteNumber' to the console.
...
```

If everything works properly, then you should have a program that asks the user for a number, and outputs that number multiplied by 10.

### Arrays

just one number? boring!
can only be one type
editing requires mutable array
how to edit arrays
common array operations

<p align="right">
    <a href='Conditionals.md'>Conditionals</a>
</p>

___

<p align="center">
    <a href='../README.md'>Table Of Contents</a>
</p>
