# Higher Order Functions

## Description

Higher order functions are functions that use other functions. Javascript is a language where "functions are first-class objects." <sup>[1][1]</sup>

## Examples

```javascript
    
    let myArray = [1, 2, 3]

    let cubeValue = (val) => val ** 3

    let result = myArray.map(cubeValue)

    console.log(result) // will return [1, 8, 27]
```

In the example above the method `map()` is a higher function. It takes in the function value of cubeValue and applies it to all the values in array.

[1]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions
