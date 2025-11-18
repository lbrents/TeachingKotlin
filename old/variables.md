# Variables

A.K.A This is where the magic happens (I might just say that everytime).


### What Are Variables?

Variables are used to save values you want to use for later. Think of variables like boxes that you can use to store one item each. For example, you have something you would like to use later so you put it in a box and then give it a label to know what that box has inside. Variables are the same concept and the following code is how we create variables in Kotlin.

``` kotlin
var myVariable = 10
```

So what does this mean? Attempting the step-by-step approach again, let's break this down.

To start creating a variable, we first use the `var` keyword. After that comes what we want to name the variable, and in the example I named it "myVariable". Lastly, we then have to give that variable a value so that there is something save in the first place. Similar to variables in math, we use the equals `=` operator followed by the value we want to save to that variable. Put this all together, and we get a variable named "myVariable" that contains the value 10.

The following snippet is the general syntax used for declaring a variable where [name] is any name you would like to give to the variable and [value] is any value you would like to save to it.

``` kotlin
var [name] = [value]
```

Now what can we do with variables? The answer is (unironically) whatever your heart desires. With variables that contain numbers, we can do math and perform calculations faster that any human could. Feel free to paste this code into the main function and see exactly what it outputs.

``` kotlin
var foo = 10

// This does math with foo
print(foo - 7)
print(foo)

// This does math with foo and assigns the result back to foo
foo = foo + 7
print(foo)
```


### Way Too Many Types

...


### Arrays

...


---

### Back To [Table Of Contents](../README.md)
