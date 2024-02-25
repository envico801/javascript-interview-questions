==================== Question ====================  

### What is the output of below code

```javascript
const squareObj = new Square(10);
console.log(squareObj.area);
class Square {
  constructor(length) {
    this.length = length;
  }
  get area() {
    return this.length * this.length;
  }
  set area(value) {
    this.area = value;
  }
}
```

- 1: 100
- 2: ReferenceError  

==================== Answer ====================  

Answer: 2  
Unlike function declarations, class declarations are not hoisted. i.e, First You
need to declare your class and then access it, otherwise it will throw a
ReferenceError "Uncaught ReferenceError: Square is not defined".  
**Note:** Class expressions also applies to the same hoisting restrictions of
class declarations.

==================== Id ====================  
497

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#497-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
