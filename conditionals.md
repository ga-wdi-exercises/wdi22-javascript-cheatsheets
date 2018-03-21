# Conditionals

## Definition
Conditionals are how we tell the computer to do something if certain _conditions_ are met. You can think of them as if-then statements: If something is true, then please do this. 

Conditionals are the skeleton of programming. We also call conditionals "control flow" because we use them to manage the flow of the program. We use conditionals to create different paths a user can take in a program. 

## Syntax
The basic syntax is as follows:
``` 
if (condition) {
  // code to run when condition is true
}
```
* ```condition``` will evaluate to a boolean value. 
* ```// code to run when condition is true``` can be any code. It can output something to the console. It can return something. It can even be another conditional statement. 

That syntax covers simple if-then statements, but we often want to have more than just one option in a condition. If that's the case, we need a slightly more complex syntax:
```
if (condition) {
  // this code runs if the condition evaluates to true
}
else if (anotherCondition) {
  // this code runs if the first condition evaluates to false and anotherCondition evaluates to true
}
else {
  // this code runs if the first condition and anotherCondition evaluate to false
  // this code does not run if the condition or anotherCondition evaluates to true
}
```
* ```condition``` and ```anotherCondition``` will both evaluate to booleans -- either true or false. 
* the first ```else if``` only runs if the first condition is not met. 
* the ```else``` only runs if both the first two conditions are not met. In the program, the computer will stop whenever it reaches a true statement and run that code.

## Examples
Now let's take a look at some examples:

### Standard Else-If Statement
```
let age = 65
if (age >= 65) {
  console.log('You may be eligible for Medicare!')
} else if (age >= 26) {
  console.log('You will need to acqurie your own health insurance either from an employer or via the exchanges.')
} else {
  console.log('You are eligible to receive health insurance from your parents' plan!')
}
```
* In this example, there are three segments of the population: people 65 and over, people 26-65, and people under 26. 
* Because the computer reads the conditions sequentially, we don't need to write ```age < 65 && age >= 26```. We only need the last half of that statement
* We assume that everyone who is not over 26 is by definition under 26; however, this may not always be the case. For example, imagine of someone set ```age = "thirty"```. In this case, it would evaluate as NaN and fall under the ```else``` bucket. When writing programs, you should be aware of mistakes people might make.

### Nested Within a Conditional
```
let age = 22
let parentsHaveInsurance = 'yes'
if (age >= 65) {
  console.log('You may be eligible for Medicare!')
} else if (age >= 26) {
  console.log('You will need to acqurie your own health insurance either from an employer or via the exchanges.')
} else {
  if (parentsHaveInsurance === 'yes') {
    console.log('You can use your parents insurance!')
  } else {
    console.log('Because your parents don't have insurance, you will need to acquire it from the exchanges or an employer.')
  }
}
```
* In this example, we nested another conditional in the last step of the conditional we wrote above. This now tests whether the user has access to a parent-owned plan. If so, they can use that insurance. If not, they will have to get their own. 

### Conditional Within a Function
```
function howToGetInsurance() {
  age = prompt('What is your age')
  parentsHaveInsurance = prompt('Do your parents have insurance? yes/no')
  if (age >= 65) {
    console.log('You may be eligible for Medicare!')
  } else if (age >= 26) {
    console.log('You will need to acqurie your own health insurance either from an employer or via the exchanges.')
  } else {
    if (parentsHaveInsurance === 'yes') {
      console.log('You can use your parents insurance!')
    } else {
      console.log('Because your parents don't have insurance, you will need to acquire it from the exchanges or an employer.')
  }
}
}
```
* This uses the same example as above but nests it within a function ```howToGetInsurance```, which asks the user for their age and whether their parents have insurance and gives them an answer in the console.