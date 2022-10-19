# Operators and Conditions

## Arithmatic Operators

Add, Subtract, Multiply, Divide, and Modulus

``` swift
var one = 1
var two = 2

let sum = one + two
let difference = one - two
let product = one * two
let quotient = one / two
let remainder = one % two
```

## Operator Overloading

What an operator does depends on the values given.

Adding intergers.
``` swift
let three = 1 + 2

// output: 3
```

Joining strings.
``` swift
let newStr = "Joined" + "String."

// output: Joined String.
```

Joining arrays.
``` swift
let firstHalf = ["One", "Two"]
let secondHalf = ["Three", "Four"]
let numArr = firstHalf + secondHalf

// output: ["One", "Two", "Three", "Four"]
```

## Compound Assignment Operators

Shorthand for operators +, -, *, /, %.

``` swift
var num = 1
num += 2 // += 2 is the same as num = num + 2

// output: 3
```

## Comparison Operators

| Operator | Meaning                  |
| :------- | :----------------------- | 
| `==`     | equals                   |
| `!=`     | not equals               |
| `>`      | greater than             |
| `<`      | less than                |
| `>=`     | greater than or equal to |
| `<=`     | less than or equal to    |
```
let one = 1
let two = 2

one == two // false
one != two // true
one > two // false
one < two // true
```

Also works with strings since they have a nature alphabetical order.
``` swift
"abc" < "def" // true
```

## Conditions

`if` statements can be use to branch code based on conditions.
`else if` is used to chain if statements.
`else` is ran if the condition is false.

``` swift
let num1 = 1
let num2 = 2

if num1 > num2 {
    print(num1)
} else if num1 < num2 {
    print(num2)
} else {
    print(num1 + " = " num2)
}
```

## Combining Conditions

We can use `&&` (and) and `||` (or) to combine conditions.

``` swift
let num1 = 1
let num2 = 3

if num1 < 4 && num2 < 4 {
    print("Both are less than 4")
} 

if num1 < 3 || num2 < 3 {
    print("At least one is less than 3")
}
```

## Ternary Operator

We can use ternary operator to store a value based on a condition.

Format:
`var example = conditional statement : value if true ? value if false`

``` swift
let num1 = 1
let num2 = 2

var equalNum = num1 == num2 ? "Numbers are equal." : "Numbers are not equal."

// output: Numbers are not equal.
```

# Switch Statement

`Switch` statements can be used when you have a lot of different conditions as it is clear than if/else statments with readability.

We use `default` in case our switch value does not match any of the cases.

``` swift
let weather = "sunny"

switch weather {
case "rain":
    print("Bring an umbrella")
case "snow":
    print("Wrap up warm")
case "sunny":
    print("Wear sunscreen")
default:
    print("Enjoy your day!")
}

// output: Wear sunscreen
```

We can use `fallthrough` to continue executing through cases rather than stopping was we find a matching case. 

``` swift
let weather = "sunny"

switch weather {
case "rain":
    print("Bring an umbrella")
case "snow":
    print("Wrap up warm")
case "sunny":
    print("Wear sunscreen")
    fallthrough
default:
    print("Enjoy your day!")
}

// output: 
// Wear sunscreen
// Enjoy your day!
```

## Range Operators

Swift offers `..<` and `...` as ranger operators.

`..<` is excludes the final value. 
``` swift
1..<5 // 1, 2, 3, 4
```

`...` is inclusive of final value. 
``` swift
1...5 // 1, 2, 3, 4, 5
```