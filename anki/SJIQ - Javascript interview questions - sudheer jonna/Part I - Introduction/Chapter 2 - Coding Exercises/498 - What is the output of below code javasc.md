========== Question ==========  

### What is the output of below code

```javascript
function Person() {}
Person.prototype.walk = function () {
    return this;
};
Person.run = function () {
    return this;
};
let user = new Person();
let walk = user.walk;
console.log(walk());
let run = Person.run;
console.log(run());
```

-   1: undefined, undefined

-   2: Person, Person

-   3: SyntaxError

-   4: Window, Window  

========== Answer ==========  

Answer: 4

When a regular or prototype method is called without a value for **this**, the methods return an initial this value if the value is not undefined. Otherwise global window object will be returned. In our case, the initial `this` value is undefined so both methods return window objects.

========== Id ==========  
498

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#498-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
