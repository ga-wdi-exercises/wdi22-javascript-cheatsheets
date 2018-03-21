# Functions

### About
* A function is a block of reusable Javascript code or statement that can be called from anywhere in our program.

* Thus, a function allows for the statements inside of it to _not_ be written over and over again.

    #### Summary: Function is a reusable & "DRY" block of Javascript code.
              
                         So, stay DRY: "Don't Repeat Yourself."


### Function Reusability and DRYness Example

Let's say there is a program that calculates Amazon's shipping fees.
If the total order amount is below $25, there will be a $3 shipping fee.
If the total order amount is above $25, shipping is free!

Using, conditional statements, this how our code would look:


```let product = "Fruit Loops"
let orderAmount = 3
console.log('Thank you for ordering ' + 'product');
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

_STOP_ : given that Amazon has over thousands of products, _we can't be writing out conditionals for each product_.

#### This is where a function comes in:

```
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

```function order () {
}

// This is what we call function container
// Here "order" is the name of the function
// The parenthesis is designated for *optional* parameters/arguments
```

#### Input (Arguments or Parameters)


```function order (product, orderAmount) {
}

// Here we have an a parameter (product, orderAmount)
// Inputs are optional. The function will still work without it.
```

#### Output and side Effects

```
function order (product, orderAmount) {
  console.log('Thank you for ordering ' + product + '.')
  return 'Congrats on your purchase!'

// What the console shows is essentailly what we call a side effect. It doesn't exist outside the function.

// The Output in this case is 'Congrats on your purchase!' noted by the keyword "return." It's what the function evaluates to.
}

```
