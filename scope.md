# Scope

An important concept in JavaScript development. There are generally two types of scope: Local Scope and Global Scope. <sup>[1][1],[2][2]</sup>

## Local Scope

Variables and functions declared within an object or function are locally scoped to that function.

## Global Scope

Anything else that isn't locally scoped to another function or object is part of the global scope.

## Gotchas
Here are some things you should look out for:

Declaring variables without using var, let, or const.

```javascript

    let testFunction = function () {

        let varDelaredCorrectly = 'doneRight'

        varDeclaredIncorrectly = 'doneWrong'

        return ""
    }

    console.log(varDeclaredCorrectly)  // will send error, as it is correctly scoped to the function


    console.log(varDeclaredInCorrectly)  // will yield 'doneWrong', as it is now scoped globally
```


[1]: https://www.w3schools.com/js/js_scope.asp
[2]: https://www.sitepoint.com/demystifying-javascript-variable-scope-hoisting/
