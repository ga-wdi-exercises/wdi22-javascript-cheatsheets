# JavaScript Objects

Objects are a collection of properties, or key/value pairs.  
Objects are created using object literal notation. Use camelCase when creating object keys and add a comma after each key/value pair. You can add a comma after the last key/value pair, but best practice is to not have one.  
Here is an example of an object created using **Object Literal Notation**:  
```
var dog = {
  name: 'Fido',
  age: 5,
  favoriteTreat: 'bone',
  favoriteToy: 'ball',
  enemy: 'cat'
}
```
Objects are a complex data type and sometimes referred to as an unordered list or dictionary - with the key representing the word and the value representing the definition.  

Another way creating objects is to use the **Object Constructor Method** ```(var myObj = new Object() )```  
While we will **not** be using this method, here is an example:  
```
var dog = new Object()
  dog.name = 'Fido',
  dog.age = 5,
  dog.enemy = 'cat'
```  
Object proerties can be accessed throught dot .property or bracket ['property'] notation.  
```
console.log(dog.enemy)
console.log(dog ['enemy']) 
```
You can update the value of an object property by accessing it and assigning it a new value.
```
dog.enemy = 'postman'
dog ['enemy'] = 'postman'
```
You can add properties to objects in a similar fashion.
```
dog.trick = 'roll over'
```
Deleting an object property removes the whole key/value pair, not just the value.   
```
delete dog.enemy
```

Objects can also include nested collections such as arrays and other objects.
```
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
  }
}
```
Accessing nested collections through dot notiation:
```
console.log(dog.enemies[0])
//returns 'cat'
console.log(dog.vet.phone)
//returns '222-333-4444'