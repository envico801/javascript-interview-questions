==================== Question ====================  

### How do you call the constructor of a parent class  

==================== Answer ====================  

You can use the `super` keyword to call the constructor of a parent class.
Remember that `super()` must be called before using 'this' reference. Otherwise
it will cause a reference error. Let's the usage of it,

```javascript
class Square extends Rectangle {
  constructor(length) {
    super(length, length);
    this.name = 'Square';
  }
  get area() {
    return this.width * this.height;
  }
  set area(value) {
    this.area = value;
  }
}
```

==================== Id ====================  
257

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#257-How-do-you-call-the-constructor-of-a-paren

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
