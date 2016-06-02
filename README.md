# Array

![Jake](https://media.giphy.com/media/lUQxdO6Y7Vmx2/giphy.gif)

> Dude, suckin' at something is the first step towards being sorta good at something

## Learning Objectives - The student should be able to..

* Explain that an `Array` is a type, similar to how name is of type `String` in the following code snippet:
 
```swift
let name: String = "Dr. Alan Grant"
```

* Explain that `Array` is a *collection type* and that `Array`'s are ordered collections of values.
* Explain that *mutable* means that you can change (or *mutate*) the collection **after** it is created by adding, removing, or changing items in the collection. This is done so using `var` in the declaration.
* Explain that *immutable* means that the collections size and contents **cannot** be changed. This is done so using `let` in the declaration.
* Can create an array as follows and describe this as declaring an array of type `[String]` which contains two `String` literal values ("Eggs & "Milk").

```swift
var shoppingList = ["Eggs", "Milk"]
```
* Can access the values inside of an Array using *subscript syntax*.  

```swift
let itemAtIndexZero = shoppingList[0]
let itemAtIndexOne = shoppingList[1]

print(itemAtIndexZero)
// prints "Eggs"

print(itemAtIndexOne)
// prints "Milk"
```

* Can change an existing value at a given index using subscript syntax:

```swift
shoppingList[0] = "Peanut Butter"

print(shoppingList)
// prints "["Peanut Butter", "Milk"]"
```



## What the student can do at this point 

* Create variables and constants
* Is familiar with type annotations, type inference and string interpolation.
* Can create functions with return types.
* Is familiar with the `String`, `Int`, `Double`, and `Bool` type.
* Can perform arithmetic operations on `Int` and `Double`.
* Understands `if` and `else clause` statements.



## Outline / Notes

*  I like the idea of introducing Array's by referring to a shopping list, it's what Apple did in their documentaiton and I think... if the student is to then read along with the Apple documentation after reading the multiple units on Collections - it will help for them to see it again (I think).
* The following is what I would like to expose to the student in this readme:

```swift
var shoppingList = ["Barbecue sauce", "Dark rum", "Honey", "Pork tenderloin", "Hamburger buns"]
// Here we're declaring an array named shoppingList2 of type [String] with five String values.

print(shoppingList)
// prints "["Barbecue sauce", "Dark rum", "Honey", "Pork tenderloin", "Hamburger buns"]"


var shoppingList2: [String] = ["Cookie mix", "Milk" ]
// Here we're declaring an array named shoppingList2 of type [String] with two String values, "Cookie mix" & "Milk".


var shoppingList3: Array<String> = ["Cookie dough", "Icecream"]
// Here we're declaring an array named shoppingList3 of type [String] with two String values, "Cookie dough" & "Icecream".


var shoppingList4: [String]

shoppingList4 = ["Vanilla", "Pancakes", "Milk"]
// Here we're declaring an array named shoppingList4 of type [String] with two String values then in the following line initializing it with three String values, "Vanilla", "Pancakes" and "Milk".
```
* I don't think we should dwell too much on `Array<String>`. This will be the first time they see `Array`'s so I think it's more important that they understand WHY they are using `Array`'s and WHAT problem does using `Array`'s solve. 
* Also, could they make an `Array` of `Int`'s? YES!
* I want them to be able to understand all of the following, so it should be broken down into pieces and explained thoroughly, making no assumptions explaining everything in great detail:

```swift
var myShoppingList = ["Peanut Butter", "Jelly", "Bread", "Strawberries"]

myShoppingList.append("Bananas")

print(myShoppingList)
// prints "["Peanut Butter", "Jelly", "Bread", "Strawberries", "Bananas"]"
``` 
* This should also be explained in detail, formulating a sentence as to what is going on that way the student can see the proper way to structure a sentence as to what's happening here. This will help them be able to Google things as well as challenge them to see if they REALLY do understand what they're seeing:

```swift
myShoppingList[0] = "Almond Butter"

let firstItem = myShoppingList[0]

print(firstItem)
// prints "Almond Butter"

print(myShoppingList)
// prints "["Almond Butter", "Jelly", "Bread", "Strawberries", "Bananas"]"
```

* Challenge the student to write a function that takes in an `Array` as an argument, the `Array`'s type is `[String]`, where they are asked to grab the first element in the array (at index 0) and see if it's value is equal to "Bread". If so, return `true`.. if not, return `false`.

<a href='https://learn.co/lessons/Array' data-visibility='hidden'>View this lesson on Learn.co</a>
