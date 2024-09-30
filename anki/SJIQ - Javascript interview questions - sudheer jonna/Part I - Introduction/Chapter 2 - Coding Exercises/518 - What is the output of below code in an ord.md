========== Question ==========  

### What is the output of below code in an order?

```javascript
function second() {
    var message;
    console.log(message);
}
function first() {
    var message = 'first';
    second();
    console.log(message);
}
var message = 'default';
first();
console.log(message);
```

-   1: undefined, first, default

-   2: default, default, default

-   3: first, first, default

-   4: undefined, undefined, undefined  

========== Answer ==========  

Answer: 1

Each context(global or functional) has it's own variable environment and the callstack of variables in a LIFO order. So you can see the message variable value from second, first functions in an order followed by global context message variable value at the end.

========== Id ==========  
518

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#518-What-is-the-output-of-below-code-in-an-ord

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
