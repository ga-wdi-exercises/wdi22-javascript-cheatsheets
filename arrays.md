#_**Introduction to Arrays**_

### Arrays are a collection of global related data types and are ordered in an organized index. They are used to implement a ton of other data structures – like queues, stacks, lists, and sometimes strings. There are many ways you can use arrays to manipulate your program, but we will simply state here what they are.

```js
Example: x = [1, 2, 3]
```

In order to understand what an array is, you *must* understand that indexing in an array begins at 0. **In other words, the first element will begin at "0", the second element in an array will be put as "1", and so on.** Arrays are used to access elements.

### _*Creating an Array*_ Using an array literal is the easiest way to create a JavaScript Array. 

*Syntax:* 
You want to declare a variable of your desired array type. 

**Note: Before 2015, you were limited to only using *var* as the declaration of your variable. But now, you may use *let* and *const*. There are subtleties that differentiate between the three.**


let/const/var **array_name** = [item1, item2, ...]; 

Spaces and line breaks are not important. A declaration can span multiple lines: 

*Ex:* 

```js 
var cars = [ "Saab", "Volvo", "BMW" ];
``` 

###Access the Elements of an Array 

You refer to an array element by referring to the index number. 

*This statement accesses the value of the first element in cars:* 

```js 
var name = cars[0]; 
This statement modifies the first element in cars: cars[0] = "Opel";
```

*Example* 

```js
var cars = ["Saab", "Volvo", "BMW"]; document.getElementById("demo").innerHTML = cars[0];
```

###*Array Properties and Methods* 

The real strength of JavaScript arrays are the built-in array properties and methods: 

*Examples* 

```js
var x = cars.length; // The length property returns the number of elements var y = cars.sort(); // The sort() method sorts arrays Array methods are covered in the next chapters. 
```

###*The length Property* 

The length property of an array returns the length of an array (the number of array elements). 

*Example* 


```js
Js var fruits = ["Banana", "Orange", "Apple", "Mango"]; fruits.length; 
// the length of fruits is 4 
```


###*Looping Array Elements* 

The best way to loop through an array, is using a "for" loop: 

*Example* 


```js 
var fruits, text, fLen, i; fruits = ["Banana", "Orange", "Apple", "Mango"]; fLen = fruits.length; text = "<ul>"; for (i = 0; i < fLen; i++) { text += "<li>" + fruits[i] + "</li>"; }
```