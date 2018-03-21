# Primitive Data Types

According to Mozilla MDN there are now 7 data types in ES6 (ES2015). <sup>[1][1]</sup>


Those data types are as follows:

|||
|-|:---|
| Strings | Ex: "string" |
| Number | Ex: 7|
| Undefined | The type of any variable that has not been assigned a type|
| Null | Data type with only one value `null`.|
| Boolean | Ex: true, or false (includes truthy and falsy values) |
| Symbol | .. (Note: I"m not sure when symbol will be used.) |
| Object| |

## Type Descriptions

### Strings
Strings contain text. They are typically written with quotes:
```js
typeof("hi, this is a string") // this is a string
```

### Number
Numbers are just like they sound. They are numbers. There is only one number type. However, there are a few tricky exceptions:
```js
typeof(10) // this is a number
typeof("10") // this is a string
"10" === 10 // this will evaluate false because 10 and "10" are not of the same data type
"10" == 10 // this will evaluate true because the double == only checks if the value are the same while ignoring data types
typeof(NaN) // NaN means 'Not a Number' but it will evaluate as a number.
```

### Undefined
Any variable has been declared, but not yet assigned a value will be a 'undefined.'

### Null
Null is nothing. It is empty. In contrast, Undefined is waiting for a value. It is a type with only one value. <sup>[1][1]</sup>

### Boolean
A variable with a type of boolean will either be true, false, "truthy" or "falsy." True and false values are self explanatory. Truthy and falsy require more explanation.

Variables with value of '0' and 'null' are considered falsy. 
MDN contains a more complete list. <sup>[2][2]</sup>

```javascript
  if (false)
  if (null)
  if (undefined)
  if (0)
  if (NaN)
  if ('')
  if ("")
  if (document.all) [1]
```
All the values above will evaluate to false.

### Collection
Collections can be [arrays](arrays.md) or [objects](objects.md). You can click on the link to learn more about them. 

## Determining the type of variable
We use `typeof <var>` to determine the type of a variable.



[1]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures
[2]: https://developer.mozilla.org/en-US/docs/Glossary/Falsy