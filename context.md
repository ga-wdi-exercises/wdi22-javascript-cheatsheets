# **Context**

Context is the object that a function is attached to.


When a Javascript function is invoked, a context is set.  The context will be the same value of the object that owns the running code at that moment.  The value can be referenced with `this`.  Basically, `this` is a substitute for the object in question.


### example
```javascript
var person = {
  firstName: "Stephen",
  lastName: "Hawking",
  fullName: function () {
    console.log(this.firstName + " " + this.lastName);
    //which is the same as
    console.log(person.firstName + " " + person.lastName);
  }
}
```
In the example, the object that the method is being called on is `person`

`this` is not assigned a value until an object invokes the function where `this` is defined.  If you are unsure where `this` is at a given point in your code.
```javascript
console.log(this)
```