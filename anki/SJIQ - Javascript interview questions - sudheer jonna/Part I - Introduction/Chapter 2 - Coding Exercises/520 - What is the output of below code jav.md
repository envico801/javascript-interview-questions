==================== Question ====================  

### What is the output of below code

```javascript
const user = {
  name: 'John',
  eat() {
    console.log(this);
    var eatFruit = function () {
      console.log(this);
    };
    eatFruit();
  },
};
user.eat();
```

- 1: {name: "John", eat: f}, {name: "John", eat: f}
- 2: Window {...}, Window {...}
- 3: {name: "John", eat: f}, undefined
- 4: {name: "John", eat: f}, Window {...}  

==================== Answer ====================  

Answer: 4  
`this` keyword is dynamic scoped but not lexically scoped . In other words, it
doesn't matter where `this` has been written but how it has been invoked really
matter. In the above code snippet, the `user` object invokes `eat` function so
`this` keyword refers to `user` object but `eatFruit` has been invoked by `eat`
function and `this` will have default `Window` object.  
The above pit fall fixed by three ways,

1. In ES6, the arrow function will make `this` keyword as lexically scoped.
   Since the surrounding object of `this` object is `user` object, the
   `eatFruit` function will contain `user` object for `this` object.

```javascript
const user = {
  name: 'John',
  eat() {
    console.log(this);
    var eatFruit = () => {
      console.log(this);
    };
    eatFruit();
  },
};
user.eat();
```

The next two solutions have been used before ES6 introduced.  
2. It is possible create a reference of `this` into a separate variable and use
that new variable inplace of `this` keyword inside `eatFruit` function. This is
a common practice in jQuery and AngularJS before ES6 introduced.

```javascript
const user = {
  name: 'John',
  eat() {
    console.log(this);
    var self = this;
    var eatFruit = () => {
      console.log(self);
    };
    eatFruit();
  },
};
user.eat();
```

3. The `eatFruit` function can bind explicitly with `this` keyword where it
   refers `Window` object.

```javascript
const user = {
  name: 'John',
  eat() {
    console.log(this);
    var eatFruit = function () {
      console.log(this);
    };
    return eatFruit.bind(this);
  },
};
user.eat()();
```

==================== Id ====================  
520

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#520-What-is-the-output-of-below-code-jav

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
