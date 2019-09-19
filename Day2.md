Day 2 of Swift 

Today I learned:

1. Arrays
let john = "John Lennon"
let paul = "Paul McCartney"
let george = "George Harrison"
let ringo = "Ringo Starr"

let beatles = [john, paul, george, ringo]

beatles[1]

2. Sets
let colors = Set(["red", "green", "blue"])

Sets are collections of values just like arrays, except they have two differences:

Items aren’t stored in any order; they are stored in what is effectively a random order.
No item can appear twice in a set; all items must be unique.

3. Tuples
var name = (first: "Taylor", last: "Swift")

name.0 
name.first

Tuples allow you to store several values together in a single value. That might sound like arrays, but tuples are different:

You can’t add or remove items from a tuple; they are fixed in size.
You can’t change the type of items in a tuple; they always have the same types they were created with.
You can access items in a tuple using numerical positions or by naming them, but Swift won’t let you read numbers or names that don’t exist.

4. Arrays vs Sets vs Tuples
Tuple : If you need a specific, fixed collection of related values where each item has a precise position or name,
Set: If you need a collection of values that must be unique or you need to be able to check whether a specific item is in there extremely quickly
Array: If you need a collection of values that can contain duplicates, or the order of your items matters

5. Dictionaries
let heights = [
"Taylor Swift": 1.78,
"Ed Sheeran": 1.73
]

heights["Taylor Swift"]

6. Dictionary Default values
let favoriteIceCream = [
"Paul": "Chocolate",
"Sophie": "Vanilla"
]

favoriteIceCream["Charlotte", default: "Unknown"]

7. Create empty collections
Empty Dictionary: var teams = [String: String]()
var scores = Dictionary<String, Int>()

Empty Array: var results = [Int]()

Empty Set: var words = Set<String>()


8. Enumurations
enums – are a way of defining groups of related values in a way that makes them easier to use.

enum Result {
case success
case failure
}

let result4 = Result.failure

9. Enum Associated values
enum Activity {
case bored
case running(destination: String)
case talking(topic: String)
case singing(volume: Int)
}

let talking = Activity.talking(topic: "football")

10. Enum Raw values
enum Planet: Int {
case mercury
case venus
case earth
case mars
}

Swift will automatically assign each of those a number starting from 0, and you can use that number to create an instance of the appropriate enum case.

enum Planet: Int {
case mercury = 1
case venus
case earth
case mars
}

