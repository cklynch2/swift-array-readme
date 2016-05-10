# Array

![Jurassic Park](https://www.gapyear.com/images/advertiser_files/5578279cf178e.jpg)

## Learning Objectives - The student should be able to..

* Explain that an `Array` is a type, similar to how name is of type `String` in the following code snippet:
 
```swift
let name: String = "Dr. Alan Grant"
```

* Explain that `Array` is a *collection type* and that `Array`'s are ordered collections of values.
* Explain that *mutable* means that you can change (or *mutate*) the collection **after** it is created by adding, removing, or changing items in the collection. This is done so using `var` in the declaration.
* Explain that *immutable* means that the collections size and contents **cannot** be changed. This is done so using `let` in the declaration.
* Can create an array as follows. I'm unsure of the exact style to introduce to the student here, do we do it like so (is this *best* practice?).

```swift
var clonedDinosaurs = [
    "Tyrannosaurus rex",
    "Velociraptor",
    "Triceratops",
]
```



## What the student can do at this point 

* Create variables and constants
* Is familiar with type annotations, type inference and string interpolation.
* Can create functions with return types.
* Is familiar with the `String`, `Int`, `Double`, and `Bool` type.
* Can perform arithmetic operations on `Int` and `Double`.
* Understands `if` and `else clause` statements.



## Outline / Notes

*  I like the idea of putting the student in the mind of someone running Jurassic Park. If they want to keep track of the dinosaurs they've cloned (so far), how can they do that? With an `Array`.
* The following is what I would like to expose to the student in this readme:

```swift
var clonedDinosaurs = [
    "Tyrannosaurus rex",
    "Velociraptor",
    "Triceratops"
]

var clonedDinosaurs2: [String] = [
    // dinosaurs
]

var clonedDinosaurs3: Array<String> = [
    // dinosaurs
]

var clonedDinosaurs4: [String]
clonedDinosaurs4 = [
    // dinosaurs
]
```
* I want them to be able to understand all of the following, so it should be broken down into pieces and explained thoroughly, making no assumptions explaining everything in great detail:

```swift
clonedDinosaurs.append("Stegosaurus")
print(clonedDinosaurs)
// prints "["Tyrannosaurus rex", "Velociraptor", "Triceratops", "Stegosaurus"]"

clonedDinosaurs[0] = "T-rex"
let firstDino = clonedDinosaurs[0]
print(firstDino)
// prints "T-rex"
``` 
* Challenge the student to write a function that takes in an `Array` as an argument, the `Array`'s type is `[String]`, where they are asked to grab the first element in the array (at index 0) and see if it's value is equal to "T-rex". If so, return `true`.. if not, return `false`. The student might not know at this point what `==` is or what it does, it might have to be introduced the for the first time here (OR it might have already been introduced when we first bring up `if` statments which is a lab or two prior to this one). 

<a href='https://learn.co/lessons/Array' data-visibility='hidden'>View this lesson on Learn.co</a>
