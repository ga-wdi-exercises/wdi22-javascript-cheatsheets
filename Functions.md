# Functions

### Definition 
* A function is a block of reusable Javascript code or statement that can be called from anywhere in our program.

* Thus, a function allows for the statements inside of it to _not_ be written over and over again.

* Using functions, you can group [loops](loops.md) and [arrays](arrays.md).

    #### Summary: Function is a reusable & "DRY" block of Javascript code.
              
                         So, stay DRY: "Don't Repeat Yourself."


### Function Reusability and DRYness Example

Let's say there is a program that calculates Amazon's shipping fees.
If the total order amount is below $25, there will be a $3 shipping fee.
If the total order amount is above $25, shipping is free!

Using, conditional statements, this how our code would look:


``` js
let product = "Fruit Loops"
let orderAmount = 3
console.log('Thank you for ordering ' + product)
if (orderAmount >= 25) {
console.log('There is no shipping charge for orders over $25.00')
} else {
console.log('There will be a $3.00 shipping charge for this order')
}

let product = "MacBook Pro"
let orderAmount = 1200
console.log('Thank you for ordering ' + product);
if (orderAmount >= 25) {
console.log('There is no shipping charge for orders over $25.00')
} else {
console.log('There will be a $3.00 shipping charge for this order')
}

```

_STOP_ : given that Amazon has over thousands of products, _we can't be writing out [conditionals](conditionals.md) for each product_.

#### This is where a function comes in:

``` js
function order (product, orderAmount) {
  console.log('Thank you for ordering ' + product + '.');
if (orderAmount >= 25) {
console.log('There is no shipping charge for orders over $25.00')
} else {
console.log('There will be a $3.00 shipping charge for this order')
}
}

order('Fruit Loops', 3)
order('Mackbook Pro', 1200)

```

Thus, instead of writing a conditional for each product, all we need to do is call one function. In this case:

```order(product, orderAmount)```



## Components of a function

So, How exactly do we create functions?

Let's break down our previous example to go over how to create a function.

#### Function Container

```js
function order () {
// This is what we call function container
// Here "order" is the name of the function
// The parenthesis is designated for *optional* parameters/arguments
}

```

_Side Note_ : Naming convention is important. Make sure you give your function a name that describes what it does. Keep it short, and use camelCase.

#### Input (Arguments or Parameters)


```js

function order (product, orderAmount) {
    // Here we have an a parameter (product, orderAmount)
// Inputs are optional. The function will still work without it.
}

```

#### Output and side Effects

```js
function order (product, orderAmount) {
  console.log('Thank you for ordering ' + product + '.')
  return 'Congrats on your purchase!'

// What the console shows is essentailly what we call a side effect. It doesn't exist outside the function.

// The Output in this case is 'Congrats on your purchase!' noted by the keyword "return." It's what the function evaluates to.
}

```

#### Calling a Function

Once we defined our function, we call or invoke it by using the function name followed by parentheses.

Example:

``` js
function order (product, orderAmount) {
  console.log('Thank you for ordering ' + product + '.')
  return 'Congrats on your purchase!'
}
  order (product, orderAmount)
```

To call a function with no input, just put the function name, followed empty a parentheses

```js
function order ()) {
  console.log('Thank you for ordering ' + product + '.')
  return 'Congrats on your purchase!'
}
  order ()
```

## Defining a Function

 There are two ways to define a function: we can _declare_ it or _express_ it. 
 Let's use our previous example again.


#### Declaration

```js
function order (product, orderAmount) {
}
```
Function declaration defines a function without assigning it a variable.


#### Expression

```js
let order = function  (product, orderAmount) {
}
```
Functio expression on the other hand, defines a function by _assigning_ it to a variable. Here, our function is assigned to the variable "Order."


Although, function declaration and expressions accomplish the same thing, but are processed differently.



## Hoisting

Hoisting is when function declaration is processed before any code is executed.


#### Example: Function Declaration

```js

order ('Fruit Loops', 3)
function order (product, orderAmount) {
  console.log('Thank you for ordering ' + product + '.')
  return 'Congrats on your purchase!'
}
//Function Declaration
```
In this example, when our code runs, _the function declaration_ is processed *first*. Everything eles runs after from top to bottom. Thus, even if we call the function "order" before defining it, our code still runs.


#### Example: Function Expression

```js

order ('Fruit Loops', 3)
let order = function (product, orderAmount) {
  console.log('Thank you for ordering ' + product + '.')
  return 'Congrats on your purchase!'
}
// Function Expression
```
In this example, we get an error message


### Note: 
 Hoisting applies only to declarations, not initializations.


-_Declaration_ : When the variable is introduced.

-_Initalization_ : When a value is assigned to a variable


### Works Cited
- [MND](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting)

