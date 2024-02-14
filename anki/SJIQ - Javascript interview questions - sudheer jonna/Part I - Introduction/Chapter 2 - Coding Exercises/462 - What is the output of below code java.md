==================== Question ====================  

### What is the output of below code

```javascript
const arrowFunc = () => arguments.length;
console.log(arrowFunc(1, 2, 3));
```

- 1: ReferenceError: arguments is not defined
- 2: 3
- 3: undefined
- 4: null  

==================== Answer ====================  

Answer: 1  
Arrow functions do not have an `arguments, super, this, or new.target` bindings.
So any reference to `arguments` variable tries to resolve to a binding in a
lexically enclosing environment. In this case, the arguments variable is not
defined outside of the arrow function. Hence, you will receive a reference
error.  
Where as the normal function provides the number of arguments passed to the
function

```javascript
const func = function () {
  return arguments.length;
};
console.log(func(1, 2, 3));
```

But If you still want to use an arrow function then rest operator on arguments
provides the expected arguments

```javascript
const arrowFunc = (...args) => args.length;
console.log(arrowFunc(1, 2, 3));
```

==================== Id ====================  
462
<!--ID: 1707879784938-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#462-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
