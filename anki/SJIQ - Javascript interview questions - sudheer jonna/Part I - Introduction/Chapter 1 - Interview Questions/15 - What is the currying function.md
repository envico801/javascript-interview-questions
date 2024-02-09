==================== Question ====================  

### What is the currying function  

==================== Answer ====================  

Currying is the process of taking a function with multiple arguments and turning
it into a sequence of functions each with only a single argument. Currying is
named after a mathematician **Haskell Curry**. By applying currying, an n-ary
function turns into a unary function.  
Let's take an example of n-ary function and how it turns into a currying
function,

```javascript
const multiArgFunction = (a, b, c) => a + b + c;
console.log(multiArgFunction(1, 2, 3)); // 6
const curryUnaryFunction = (a) => (b) => (c) => a + b + c;
curryUnaryFunction(1); // returns a function: b => c =>  1 + b + c
curryUnaryFunction(1)(2); // returns a function: c => 3 + c
curryUnaryFunction(1)(2)(3); // returns the number 6
```

Curried functions are great to improve **code reusability** and **functional
composition**.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#15-What-is-the-currying-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
