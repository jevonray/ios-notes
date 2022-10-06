# Loops

## For Loops

We can use `for` loops to loop over ranges and arrays.

```
let nums = 1..10

for i in nums {
    print(i)
}
```

```
let nums = [1, 2, 3, 4, 5]

for i in nums {
    print(i)
}
```

Swift can use `_` in loops if we don't need to use the value.

```
for _ in 1...5 {
    print("This will print 5 times")
}
```

## While Loops

Similar to for loops, `while` loops are given a condition and loop until the condition is false.

```
var num = 1

while num <= 20 {
    print("This will loop until num is greater than 20")
    num += 1
}
```

## Repeat Loops

Similar to while loops, `repeat` loops check the condition at the end whereas while loops check at the start.

```
var num = 1

repeat {
    print("This will loop until num is greater than 20")
    num += 1
} while num <= 20
```

## Exiting Loops

You can exit a loop using the keyword `break`.

```
var num = 1

while num <= 20 {
    if num == 5 {
        print("Exits the loop when num = 5")
        break
    }
    num += 1
}
```

## Exiting Multiple Loops

If you need to break out of a nested loop we can give the outer loop a label then call the `break` keyword with that label.

```
outerLoop: for i in 1...10 {
    for j in 1...10 {
        let product = i * j
        print ("\(i) * \(j) is \(product)")

        if product == 50 {
            print("It's a bullseye!")
            break outerLoop
        }
    }
}
```

## Skipping Items

To skip items in a loop we can use the `continue` keyword.

```
for i in 1...10 {
    if i % 2 == 0 {
        continue
    }
    print(i)
}
```

## Infinite Loops

You can use while loops to create infinite loops. It is important to still have a way for you exit the loop.

```
var counter = 0

while true {
    if counter == 100 {
        break
    }

    counter += 1
}
```