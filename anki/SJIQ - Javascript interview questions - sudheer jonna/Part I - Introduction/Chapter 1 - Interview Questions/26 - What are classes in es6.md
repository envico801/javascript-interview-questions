==================== Question ====================  

### What are classes in ES6  

==================== Answer ====================  

In ES6, Javascript classes are primarily syntactic sugar over JavaScript’s
existing prototype-based inheritance.  
For example, the prototype based inheritance written in function expression as
below,

```javascript
function Bike(model, color) {
  this.model = model;
  this.color = color;
}
Bike.prototype.getDetails = function () {
  return this.model + ' bike has' + this.color + ' color';
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
    return this.model + ' bike has' + this.color + ' color';
  }
}
```

==================== Id ====================  
26

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#26-What-are-classes-in-es6

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
