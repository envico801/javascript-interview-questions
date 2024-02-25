==================== Question ====================  

### What is the output of below code

```javascript
class Vehicle {
  constructor(name) {
    this.name = name;
  }
  start() {
    console.log(`${this.name} vehicle started`);
  }
}
class Car extends Vehicle {
  start() {
    console.log(`${this.name} car started`);
    super.start();
  }
}
const car = new Car('BMW');
console.log(car.start());
```

- 1: SyntaxError
- 2: BMW vehicle started, BMW car started
- 3: BMW car started, BMW vehicle started
- 4: BMW car started, BMW car started  

==================== Answer ====================  

Answer: 3  
The super keyword is used to call methods of a superclass. Unlike other
languages the super invocation doesn't need to be a first statement. i.e, The
statements will be executed in the same order of code.

==================== Id ====================  
499

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#499-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
