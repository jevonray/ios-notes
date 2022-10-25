# functions, Parameters, and Errors

## Writing Fuctions

Swift function start with the `func` keyword.

``` swift
func Hello() {
    let message = "Hello World!"
    print(message)
}

Hello()
```

## Accepting Parameters

Functions can accept parameters.

``` swift
func square(number: Int) {
    print(number * number)
}
```
We can calling a function with parameters we add in the variable name as well.

```swift
square(number: 9)
```

## Returning Values

We can also return values from function using the `return` keyword and specifying the return type using `->`.

``` swift
func square(number: Int) -> Int {
    return number * number
}

print(square(number: 8))
```

## Parameter Labels

Since we use parameter labels when defining and calling the function we can give them different names for internal and external use.

``` swift
func sayHello(to name: String) {
    print("Hello, \(name)!")
}

sayHello(to: "Swifty")
```

The parameter is called `to name` where `to` is the external label and `name` is the internal label.

## Omitting Parameter Labels

We can exclude a parameter label from being used externally by using `_` in place of a label.
``` swift
func sayHello(_ name: String) {
    print("Hello, \(name)!")
}

sayHello("Swifty")
```

## Default Parameters

We can use `=` to set a parameter value to give it a default value.

``` swift
func greet(_ person: String, nicely: Bool = true) {
    if nicely == true {
        print("Hello, \(person)!")
    } else {
        print("Oh no, it's \(person) again...")
    }
}

greet("Jane")
greet("Jane", nicely: false)
```

## Variadic Functions

We can pass in lots of arguments for one paramter using `...` in the function.

``` swift
func square(numbers: Int...) {
    for number in numbers {
        print("\(number) squared is \(number * number)")
    }
}

square(numbers: 1, 2, 3, 4, 5)
```

## Writing throwing functions

We can use `throw` clauses to throw errors.

``` swift
enum PasswordError: Error {
    case obvious
}

func checkPassword(_ password: String) throws -> Bool {
    if password == "password" {
        throw PasswordError.obvious
    }

    return true
}
```

## Running throwing functions

We can use `do`, `try`, and `catch` to run risky code and catch possible errors.

``` swift
do {
    try checkPassword("password")
    print("That password is good!")
} catch {
    print("You can't use that password.")
}
```

## Inout Parameters

Parameters passed into functions are constants so they cannot be changed. 
We can use `inout` which will allow us to change the parameter in the function.
When calling the function an inout variable must use `&` when passed in to denote to the user that it might be changed.

``` swift
func doubleInPlace(number: inout Int) {
    number *= 2
}

var myNum = 10 
doubleInPlace(number: &myNum)
```