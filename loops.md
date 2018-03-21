# Loops
## While Loops
### Definition and Syntax
A ```while``` loop is a way to go through a block of code until a certain condition is met. A while loop can run an infinite number of times, so it is important to be careful when using it. It is best used when you don't know how many times a piece of code will need to be run. 

The basic syntax is:
```js
while (condition) {
  // code to do
  // code to affect condition
} 
```
* ```condition`` can be anything that evaluates to a boolean, such as greater-than or equal-to statements.
* ```//code to do``` is code you want to run everytime the loop happens
* ```//code to affect condition``` is code that will impact the condition that started the loop. This prevents the loop from running forever. 

### Example
```js
while (answer != 'apple') {
  alert('please help us unscramble the letters to make a word.')
  answer = prompt('unscramble: \'ppela\'. What world could that be? Hint: it\'s a fruit')
}
```
* This example will prompt the user to unscramble "ppela" an inifinite number of times until they guess the correct answer "apple"

## For Loops
### Definition and Syntax
A ```for``` loop is a way to iterate something a specified number of times. We use this when we know how many times we will need to loop something. They are often used to iterate over arrays and objects. 

The basic syntax is:
```js
for (let i = 0; i < 100; i++) {
  //code to run on each i
}
```
* ```i = 0``` is the starting position
* ```i < 10``` is the condition. When this is true, keep looping
* ```i++``` is what we do to i after each loop. In this case, it is shorthand notation for ```i = i + 1```.
* ```//code to run on each i``` should be any code you want to apply to each ```i``` .

### Example
```js
let healthcareExchange = [
  {
    name: 'Cigna',
    premium: '$200/month',
    deductible: '$6,000'
  },
  {
    name: 'Aetna',
    premium: '$300/month',
    deductible: '$4,500'
  },
  {
    name: 'UnitedHealthcare',
    premium: '$250/month',
    deductible: '$5,000'
  },
]

for (i = 0; i < healthcareExchange.length; i++) {
  console.log(`${healthcareExchange[i].name} costs ${healthcareExchange[i].premium} with a ${healthcareExchange[i].deductible} deductible.`)
}
```
* In this example, we first declared an array of 3 objects, each with the costs of a different health insurance provider. 
* The ```for``` loop goes through and prints a sentence about each one in the console. 

## For In Loops
### Definition and Syntax
A ```for in``` loop is very similar to a for loop, but it is only for looping through an array or object. 

The basic syntax is:
```js
for (let i in collection) {
  // code to apply to each item in the array
}
```
* ```i``` refers to each item in the array
* ```array``` is any variable set to an array or object

### Example
Using the same array ```healthcareExchange``` we established before, we can run this ```for in``` loop to get the exact same output as we did previously:
```js
for (let i in healthcareExchange) {
  console.log(`${healthcareExchange[i].name} costs ${healthcareExchange[i].premium} with a ${healthcareExchange[i].deductible} deductible.`)
}
```





### How to loop through an array

You can use a *for loop* to traverse objects in an array. 

#### Example:

```js
var step;
for (step = 0; step < 5; step++) {
  // Runs 5 times, with values of step 0 through 4.
  console.log('Walking east one step');
}
```
[^fn]

[^fn]
March 13, 2018

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array