# Primitive Data Types

According to Mozilla MDN there are now 7 data types in ES6 (ES2015). <sup>[1][1]</sup>


Those data types are as follows:

|||
|-|:---|
| Strings | Ex: "string" |
| Number | Ex: 7|
| Undefined | The type of any variable that has not been assigned a type|
| Null ||
| Boolean | Ex: true, or false (includes truthy and falsy values) |
| Symbol | .. (Note: I"m not sure when symbol will be used.) |
| Object| |

## Type Descriptions

### Strings
Strings contain text.

### Number
There is only one number type

### Undefined
Any variable has been declared, but not yet assigned a value will be a 'undefined.'

### Null
A type with only one value. <sup>[1][1]</sup>

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

### Object

## Determining the type of variable
We use `typeof <var>` to determine the type of a variable.



[1]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures
[2]: https://developer.mozilla.org/en-US/docs/Glossary/Falsy