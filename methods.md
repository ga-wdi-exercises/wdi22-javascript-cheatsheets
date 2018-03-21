# JavaScript Methods  

Methods are functions that are attached to an object.  
Therefore, a method is a property that contains a function definition.  
Here's an example of methods within an object:  
```js
var dog = {
  name: 'Fido',
  age: 5,
  favoriteTreat: 'bone',
  favoriteToy: 'ball',
  trick: 'roll over',
  
  enemies: ['cat', 'postman', 'vacuum cleaner'],
 
  vet: {
    name: 'Pet Vet',
    address: '123 H St. NE',
    phone: '222-333-4444'
  },

  //methods here
  feed: function () {
    let isHungry = true 
    if (isHungry === true) {
      console.log(`It's time to feed ${dog.name}!`)
    } else {
      console.log(`Don't feed ${dog.name} right now.`)
    }
  },
  speak: function (sound) {
    console.log(`${dog.name} says ${sound}`)
  }
}
dog.feed()
//Returns 'It's time to feed Fido!'
dog.speak('woof!')  
//Returns 'Fido says woof!'
```

