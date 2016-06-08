# Array

![Jake](https://media.giphy.com/media/lUQxdO6Y7Vmx2/giphy.gif)

> Dude, suckin' at something is the first step towards being sorta good at something

## Learning Objectives - The student should be able to..

- Explain that an `Array` is a type, similar to how name is of type `String` in the following code snippet:

```swift
let name: String = "Dr. Alan Grant"
```

- Explain that `Array` is a _collection type_ and that `Array`'s are ordered collections of values.
- Explain that _mutable_ means that you can change (or _mutate_) the collection **after** it is created by adding, removing, or changing items in the collection. This is done so using `var` in the declaration.
- Explain that _immutable_ means that the collections size and contents **cannot** be changed. This is done so using `let` in the declaration.
- Can create an array as follows and describe this as declaring an array of type `[String]` which contains two `String` literal values ("Eggs & "Milk").

```swift
var shoppingList = ["Eggs", "Milk"]
```

- Can access the values inside of an Array using _subscript syntax_.

```swift
let itemAtIndexZero = shoppingList[0]
let itemAtIndexOne = shoppingList[1]

print(itemAtIndexZero)
// prints "Eggs"

print(itemAtIndexOne)
// prints "Milk"
```

- Can change an existing value at a given index using subscript syntax:

```swift
shoppingList[0] = "Peanut Butter"

print(shoppingList)
// prints "["Peanut Butter", "Milk"]"
```

## What the student can do at this point

- Create variables and constants
- Is familiar with type annotations, type inference and string interpolation.
- Can create functions with return types.
- Is familiar with the `String`, `Int`, `Double`, and `Bool` type.
- Can perform arithmetic operations on `Int` and `Double`.
- Understands `if` and `else clause` statements.

## Outline / Notes

- I like the idea of introducing Array's by referring to a shopping list, it's what Apple did in their documentaiton and I think... if the student is to then read along with the Apple documentation after reading the multiple units on Collections - it will help for them to see it again (I think).
- The following is what I would like to expose to the student in this readme:

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

- I don't think we should dwell too much on `Array<String>`. This will be the first time they see `Array`'s so I think it's more important that they understand WHY they are using `Array`'s and WHAT problem does using `Array`'s solve.
- Also, could they make an `Array` of `Int`'s? YES!
- I want them to be able to understand all of the following, so it should be broken down into pieces and explained thoroughly, making no assumptions explaining everything in great detail:

```swift
var myShoppingList = ["Peanut Butter", "Jelly", "Bread", "Strawberries"]

myShoppingList.append("Bananas")

print(myShoppingList)
// prints "["Peanut Butter", "Jelly", "Bread", "Strawberries", "Bananas"]"
```

- This should also be explained in detail, formulating a sentence as to what is going on that way the student can see the proper way to structure a sentence as to what's happening here. This will help them be able to Google things as well as challenge them to see if they REALLY do understand what they're seeing:

```swift
myShoppingList[0] = "Almond Butter"

let firstItem = myShoppingList[0]

print(firstItem)
// prints "Almond Butter"

print(myShoppingList)
// prints "["Almond Butter", "Jelly", "Bread", "Strawberries", "Bananas"]"
```

- Challenge the student to write a function that takes in an `Array` as an argument, the `Array`'s type is `[String]`, where they are asked to grab the first element in the array (at index 0) and see if it's value is equal to "Bread". If so, return `true`.. if not, return `false`.

--------------------------------------------------------------------------------

## Arrays

So far you've used variables to store `String` and `Int` values. For example, you could create a variable to represent an ingredient:

```swift
let ingredient = "Jalapeno"
```

Variables only allow you to store one item of information at a time. What if we were making a shopping list and needed all the ingredients wanted to make a sandwich?

You could create multiple variables to represent the ingredients:

```swift
let ingredient1 =  "Bread"
let ingredient2 = "Butter"
let ingredient3 = "Cheese"
let ingredient4 = "Lettuce"
let ingredient5 = "Tomatoes"
```

And then write code that passes these variables one at a time. This will get messy quickly. What if you forget an ingredient or need to add a new one? In the real world, you would write down all your ingredients on one shopping list. With Swift, like most programming languages, you achieve the same using an _array_. An array allows a variable to contain a _collection_ of values of the same type.

Arrays share similar concepts to other collection types available in Swift and you will cover these later in the course. For now it's important to know that an array is an _ordered_ collection of values, i.e. that every value has a particular place (or _index_) in the collection.

## Creating an Array

Here's how to create an array of values in Swift which represents the ingredients of a sandwich.

```swift
var list = ["Bread", "Butter", "Cheese", "Lettuce", "Tomatoes"]
```

In this case, you are creating a variable with the `var` keyword called 'list'. Swift can infer that `[String]` is the correct type for the `list` variable, based on it's content.

If you option click the `list` variable you can check Swift's guess.

![Inferred Type](inferred_type.png)

To be more precise, you can declare the type of values allowed in the array explicitly:

```swift
var shoppingList: [String] = ["Bread", "Butter", "Cheese", "Lettuce", "Tomatoes"]
```

Here you are creating a variable with the `var` keyword called 'shoppingList', setting the type of values allowed explicitly to be of `String` and then adding five string values to the array.

Or alternatively (but less used):

```swift
var shoppingList: Array<String> = ["Bread", "Butter", "Cheese", "Lettuce", "Tomatoes"]
```

To be clear, there is **no** different between this method of creating an array and the previous, but simpler method.

Often an array is initialized first and populated later. Say for example you want to make a shopping list for your weekly shop, but need to wait for your family before filling it with items.

```swift
var shoppingList: [String]

// Waiting for family to come home…
// They're back, let's make a list!

shoppingList = ["Bread", "Butter", "Cheese", "Lettuce", "Tomatoes"]
```

Here you create an array variable called 'shoppingList' that will accept values of type `String`. You then assign five string values to the variable later in the program.

## Constant Arrays

As you have used the `var` keyword in all the examples so far, these collections of values are _mutable_. This means you can add, remove or change items in the array. As with other variable types in Swift, to make an array constant, unchangeable or _immutable_, use the `let` keyword.

For example, a shopping list may change, but the ingredients for a cheese sandwich never will:

```swift
let cheeseSandwich: [String] = ["Bread", "Butter", "Cheese", "Lettuce", "Tomatoes"]
```

## Other Values in an Array

As you would expect, arrays can contain values apart from strings, and created the same way. For example, to create an array recording attendance at your Saturday afternoon sandwich meet:

```swift
var afternoonAttendance: [Int] = [10, 5, 15, 2, 12]
```

Whilst you can create arrays that contain different values, each array may only contain values of the **same** type. For example, you cannot have an array of mixed number and string values.

Try this array in a Playground and see what happens:

```swift
var mixedArray = [10, "cheese", 15, 2, "Bread"]
```

## Accessing Items in an Array

Like any series of items in a list, items in an array have a number associated with them that represents their place within it. In programming, this is called an 'index'. Remember, that whilst we start counting from 1, many programming languages start from 0, making the first item in an array actually 'at index 0'.

Continuing with our example, you want to know what the second item on the shopping list is, with a normal list this would be:

1. Bread
2. **Butter**
3. Cheese
4. Lettuce
5. Tomatoes

But, as an array starts from 0, to be precise, it's actually:

0. Bread
1. **Butter**
2. Cheese
3. Lettuce
4. Tomatoes

In the `shoppingList` array, if you want to print the value of the item in the second position, starting from 0, this is position 1\. Assign the value in that position to a variable, and print the value of the variable:

```swift
let secondItem = shoppingList[1]

print(secondItem)
// prints "Butter"
```

The syntax above is called _subscript_. The name of the array is `shoppingList` and you want to access the second item in the array by using square brackets and the position of the value, i.e. `[1]`.

## Changing Items in an Array

You have decided instead to make a ham sandwich, so you need to change the 'Cheese' value in the array. Again you need to know the position of 'Cheese' and change it by assigning a new value.

> What index is the 'Cheese' value at?

Remember, that Swift counts from '0', so the value of 'Cheese' is actually at position '2', three values into the array.

Assign the new value of 'Ham' at this index:

```swift
shoppingList[2] = "Ham"
```

If you now print the array, the values will have changed:

```swift
print(shoppingList)
// prints ["Bread", "Butter", "Ham", "Lettuce", "Tomatoes"]
```

[View this lesson on Learn.co](https://learn.co/lessons/Array)
