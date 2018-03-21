# Higher Order Functions

## Description

Higher order functions are functions that use other functions. Javascript is a language where "functions are first-class objects." <sup>[1][1]</sup>

## Examples  

### Map
```javascript
    
    let myArray = [1, 2, 3]

    let cubeValue = (val) => val ** 3

    let result = myArray.map(cubeValue)

    console.log(result) // will return [1, 8, 27]
```

In the example above the method `map()` is a higher function. It takes in the function value of cubeValue and applies it to all the values in array.

[1]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions

### For Each  
For each is also useful when you are looking to do something to every element in an array. 
```js
  let beatles = [
      {
        name: 'John',
        instrument: 'guitar'
        },       
      {
        name :'Paul',
        instrument: 'bass'
        },
      {
          name: 'George',
          instrument: 'lead guitar'
      },
      {
          name: 'Ringo',
          instrument: 'drums'
      }
]
```
Using a forEach function will perform a task on each element in the array. 
```js
  beatles.forEach(function (beatle){
      let meetBeatles = `Hello there! My name is ${beatle.name} and I play ${beatle.instrument} in The Beatles.`
      console.log(meetBeatles)
  })

// result
// Hello there! My name is John and I play guitar in the Beatles.
// Hello there! My name is Paul and I play bass in the Beatles.
// Hello there! My name is George and I play lead guitar in the Beatles.
// Hello there! My name is Ringo and I play drums in the Beatles.
```

### Filter
The higher-order function **Filter** *filters* elements from an array based on a determination of ```true``` or ```false``` for a given condition and returns them in a new array. 
```js
let myTeam = [
  {
      name: {
          first: 'Bill',
          last: 'Berry'
      },
      position: 'guard',
      avgPoints: 18,
      avgRebounds: 6
  },
  {
      name: {
          first: 'Paul',
          last: 'Westerberg'
      },
      position: 'forward',
      avgPoints: 10,
      avgRebounds: 4
  },
  {
      name: {
          first: 'Patterson',
          last: 'Hood'
      },
      position: 'forward',
      avgPoints: 12,
      avgRebounds: 7
  },
  {
      name: {
          first: 'Stephen',
          last: 'Malkmus'
      },
      position: 'center',
      avgPoints: 20,
      avgRebounds: 12
  },
  {
      name :{
          first: 'Jeff',
          last: 'Tweedy'
      },
      position: 'guard',
      avgPoints: 6,
      avgRebounds: 2
  }
]

let canScore = myTeam.filter(team => team.avgPoints >= 10)
console.log(canScore)
// Returns array of items for which avgPoints is greater than or equal to 10. In this case it is 4 items.
let canRebound = myTeam.filter(team => team.avgRebounds > 6)
console.log(canRebound)
// Returns array of items for which avgRebounds is greater than 6. In this case it is 2 items.
```