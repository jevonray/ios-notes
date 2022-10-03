# Variables, Simple Data Types, String Interpolation 

## Variables

Declaring a variable.

```
var str = "Hello World!"
```

Values of variables can be changed.

```
str = "Goodbye!"
```

## Strings

Declaring a string.

```
var str = "Hello World" 
```

## Integers

Declaring an integer.

```
var age = 38 
```

You can use underscores as separators.

```
var population = 8_000_000 
```

## Multi-line Strings

Use three doublue quotes marks (""") to declar a multi-line string.
Opening and closing quotes must be on their own lines

```
var str = """
This is a
multi-line
string.
"""
```
Output:
```
This is a 
multi-line 
string.
 ```

 To format a multi-line string without line breaks use backslash ( \\ ).

 ```
var str = """
This is a \
multi-line \
string.
"""
```
Output:
```
This is a multi-line string.
 ```

## Doubles

Doubles can hold fractional values or decimals

Declaring a double.

```
var pi = 3.14
```

## Booleans
Booleans are true or false.

Declaring a boolean.

```
var isCool = true
```

## String Interpolation

Swift can place variables inside strings.

```
var score = 85
var scoreStr = "Your score is \(score)"
```

## Constants

Declaring a constant.

```
let greeting = "Hello"
```

Unlike variables, constants cannot be modified.
We use `let` for constants and `var` for variables.

## Type Annotations

You can explicity assign a type rather than rely on Swift's type inference.

```
let greeting: String = "Hello!"
let age: Int = 38
let pi: Double = 3.14
let isCool: Bool = true
```