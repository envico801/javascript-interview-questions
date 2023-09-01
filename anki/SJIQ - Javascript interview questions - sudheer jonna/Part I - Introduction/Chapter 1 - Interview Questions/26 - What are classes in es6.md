Q: What are classes in ES6  
A: In ES6, Javascript classes are primarily syntactic sugar over JavaScript’s existing prototype-based inheritance.  
For example, the prototype based inheritance written in function expression as below,
```javascript
function Bike(model, color) {
  this.model = model;
  this.color = color;
}
Bike.prototype.getDetails = function () {
  return this.model + " bike has" + this.color + " color";
};
```
Whereas ES6 classes can be defined as an alternative
```javascript
class Bike {
  constructor(color, model) {
    this.color = color;
    this.model = model;
  }
  getDetails() {
    return this.model + " bike has" + this.color + " color";
  }
}
```
<!--ID: 1693596721172-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript #Interview

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store