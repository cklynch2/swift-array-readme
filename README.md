# Array

## Learning Objectives

* Define and create an array 
* Access items in an array
* Change items in an array

## Arrays

So far you've used variables to store `String` and `Int` values. For example, you could create a variable to represent an ingredient:

```swift
let ingredient = "Jalapeno"
```

Variables only allow you to store one item of information at a time. What if we were making a shopping list and needed all the ingredients wanted to make a sandwich?

You could create multiple variables to represent the ingredients:

```swift
let ingredient1 = "Bread"
let ingredient2 = "Butter"
let ingredient3 = "Cheese"
let ingredient4 = "Lettuce"
let ingredient5 = "Tomatoes"
```

And then write code that passes these variables one at a time. This will get messy quickly. What if you forget an ingredient or need to add a new one? In the real world, you would write down all your ingredients on one shopping list. With Swift, like most programming languages, you achieve the same using an _array_. An array allows a variable to contain a _collection_ of values of the same type.

## Creating an Array

Here's how to create an array of values in Swift which represents the ingredients of a sandwich.

```swift
var list = ["Bread", "Butter", "Cheese", "Lettuce", "Tomatoes"]
```

In this case, you are creating a variable with the `var` keyword called 'list'. Swift can infer that `[String]` is the correct type for the `list` variable, based on it's content.

Type the above into a Playground and if you option click the `list` variable you can see Swift's guess.

![Infferre](http://i.imgur.com/cO7DsAT.png)

If you wanted to be more precise when creating an array, you can declare the type of values allowed in the array explicitly:

```swift
var shoppingList: [String] = ["Bread", "Butter", "Cheese", "Lettuce", "Tomatoes"]
```

Here you are creating a variable with the `var` keyword called 'shoppingList', setting the type of values allowed explicitly to be of `String` and then adding five string values to the array.

Or alternatively (but less used):

![arrayThinga](http://i.imgur.com/RdyJI34.png)

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

![oneThing](http://i.imgur.com/DY8qbZV.png)

But, as an array starts from 0, to be precise, it's actually:

 
![zeroThing](http://i.imgur.com/d0ztePC.png)


In the `shoppingList` array, if you want to print the value of the item in the second position, starting from 0, this is position 1. Assign the value in that position to a variable, and print the value of the variable:

```swift
let secondItem = shoppingList[1]

print(secondItem)
// prints "Butter"
```

The syntax above is called _subscript_. The name of the array is `shoppingList` and you want to access the second item in the array by using square brackets and the position of the value, i.e. [1].

Arrays share similar concepts to other collection types available in Swift and you will cover these later in the course. For now it's important to know that an array is an _ordered_ collection of values, i.e. that every value has a particular place (or _index_) in the collection.

## Changing Items in an Array

You have decided instead to make a ham sandwich, so you need to change the 'Cheese' value in the array. Again you need to know the position of 'Cheese' and change it by assigning a new value.

What index is the 'Cheese' value at?

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

