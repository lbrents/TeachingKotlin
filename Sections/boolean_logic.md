# Boolean Logic

Think back to math, basic arithmetic is stuff like adding, subtracting, multiplying and dividing. These are operations that involve calculations using integers or doubles. But let me ask a question that you might not care about... What other types of calculations can we do with the other data types?

With that preface out of the way, let's introduce the type of calculations we can do with the boolean data type.

Boolean values can only be either on or off, one or zero, true or false, and so on... We can't really do anything cool with operations like addition or subtraction, so instead we have a set of different calculations we can do called boolean logic. These are helpful for when we have multiple different boolean values and we want to do certain things when they are in certain states together. That might have been worded poorly, so let's get into the code.

``` kotlin
// Some lights in a room: true = on, false = off 
var lights: Boolean = false

// The the two switches in the room
var switchA: Boolean = false
var switchB: Boolean = false
```

Here we have 3 variables, two switches and one light. Let's try a couple different situation to show what boolean logic is and how to use it.

If we want to turn on the light when both switches are on, we use the `&&` AND operator.
If we want to turn on the light when either switch is on, we use the `||` OR operator.

| Operator | A | B | Result |
| -------- | - | - | ------ |
| AND (&&) | F | F | F      |
| AND (&&) | F | T | F      |
| AND (&&) | T | F | F      |
| AND (&&) | T | T | T      |
| OR  (\|\|) | F | F | F      |
| OR  (\|\|) | F | T | T      |
| OR  (\|\|) | T | F | T      |
| OR  (\|\|) | T | T | T      |

And if we want to reverse the state of a switch, we can use the `!` NOT operator.

| Operator | A | Result |
| -------- | - | ------ |
| NOT (!)  | F | T      |
| NOT (!)  | T | F      |

Finally, let's look at this in code...

``` kotlin
// Turn on the light if switchA AND switchB are on
switchA = true
switchB = false
lights = switchA && switchB // true && false == false
println(lights)

switchA = true
switchB = true
lights = switchA && switchB // true && true == true
println(lights)

// Turn on the light if switchA OR switchB is on
switchA = false
switchB = false
lights = switchA || switchB // false || false == false
println(lights)

switchA = true
switchB = false
lights = switchA || switchB // true || false == true
println(lights)

// Turn on the light if switchA is NOT on
switchA = true
lights = !switchA // !true == false
println(lights)

switchA = false
lights = !switchA // !false == true
println(lights)
```

And that's the gist of performing calculations with booleans. There is still a lot more depth to boolean logic, but for now this is enough to do some pretty cool stuff.

Lastly, what operations are there for the other data type that result in booleans?

Hopefully this part is fairly intuitive. If not, I promise to reiterate on this later.

| Operator | Description | Example |
| -------- | ----------- | ------- |
| == | Checks if two numbers (or any datatype) are equal to each other. | 10 == 10 is True |
| != | Checks if two numbers (or any datatype) are NOT equal to each other. | 10 != 10 is False |      
| > | Checks if the first number is greater than the second. | 10 > 5 is True |
| < | Checks if the first number is lesser than the second. | 10 < 5 is False |
| <= | Checks if greater than OR equal to. | 10 >= 10 is True, 10 >= 15 is False |
| >= | Checks if lesser than OR equal to. | 10 <= 10 is True, 10 <= 15 is True |

___

[Conditionals](conditionals.md)
