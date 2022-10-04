# Complex Data Types

## Arrays

Declaring an array.
```
let apple = "apple"
let orange = "orange"
let banana = "banana"

let fruit = [apple, orange, banana]
```

Accessing an array (0 indexed).
```
fruits[1] // orange
```

Array type annotations.
```
let strArr: [String] = ["1", "2", "3", "4"]
let intArr: [Int] = [1, 2, 3, 4]
let doubleArr: [Double] = [1.0, 2.0, 3.0, 4.0]
let boolArr: [Bool] = [true, false, true, false]
```

## Sets

Sets are collections of values similar to arrays except they:
1. Elements aren't stored in any order. THey are unordered and Swift does not guarentee any order.
2. Each element must be unique.

Declaring a set.
```
let colors = Set(["red", "green", "blue"])
```

## Tuples

Tuples can store several values into a sing value.
1. You cannot add or remove items from a tuple, they are fixed in size.
2. You cannot change the type in a tuple, it stays the same as the type it was created with.
3. You can access items in tuple using numerical position or the name.

Declaring a tuple.
```
var name = (first: "Jane", last: "Doe")
```

Accessing a tuple.
```
name.0 // numerical position
name.first // name
```

## Arrays vs Sets vs Tuples 

- If you need a specific, fixed collection of related values where each item has a precise position or name, you should use a **tuple**.
- If you need a collection of values that must be unique or you need to be able to check whether a specific item is in there extremely quickly, you should use a **set**.
- If you need a collection of values that can contain duplicates, or the order of your items matters, you should use an **array**.

## Dictionaries

Dictionaries store values paired with a key.

Declaring a dictionary.
```
let heights = [
    "John": 1.73,
    "Jane": 1.54,
    "Joe": 1.68
]
```

Accessing a dictionary.
```
heights["Jane"] // output: 1.54
```

Dictionary type annotations.

First type is key type.
Second type is value type.
```
let heightDict: [String: Double]
```

## Dictionary Default Values

When trying to access a dictionary with a key that doesn't exist **nil** will be returned.

To fix this we can add a default value if the key doesn't exist.

```
heights["James", default: 1.5]
```

## Creating Empty Collections

Arrays, sets, and dictionaries are known as collections.

Creating an empty collection.
```
// Array
var fruit = [String]()
var fruit = Array<String>()

// Set
var colors = Set<String>()

// Dictionary
var heights = [String: Double]()
var heights = Dictionary<String, Double>()
```

## Enumerations

Enumeration (enums) is a way of defining groups of related values.

Defining an enum.
```
enum Results {
    case success
    case failure
}
```

Using an enum.

```
let outcome = Results.success
```

## Enum Associated Values

Enum associated values allow us to add additional details to values.
```
enum Activity {
    case bored
    case running(destination: String)
    case talking(topic: String)
    case singing(volume: Int)
}
```

```
let talking = Activity.talking(topic: "football")
```

## Enum Raw Values

Declaring enum that stores integer values.
```
enum Planet: Int {
    case mercury
    case venus
    case earth
    case mars
}
```
Swift will assign the enum values starting with 0.

Now we can assign a variable called earth to raw value 2.
```
let earth = Planet(rawValue: 2)
```

We can also assign a case a specific value and Swift will assign the rest starting with that number and counting up.
```
enum Planet: Int {
    case mercury = 1
    case venus
    case earth
    case mars
}
```
