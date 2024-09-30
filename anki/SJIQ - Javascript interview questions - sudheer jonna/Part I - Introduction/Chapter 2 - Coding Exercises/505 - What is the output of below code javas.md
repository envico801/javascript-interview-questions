========== Question ==========  

### What is the output of below code?

```javascript
let count = 10;
(function innerFunc() {
    if (count === 10) {
        let count = 11;
        console.log(count);
    }
    console.log(count);
})();
```

-   1: 11, 10

-   2: 11, 11

-   3: 10, 11

-   4: 10, 10  

========== Answer ==========  

Answer: 1

11 and 10 is logged to the console.

The innerFunc is a closure which captures the count variable from the outerscope. i.e, 10. But the conditional has another local variable `count` which overwrites the ourter `count` variable. So the first console.log displays value 11.

Whereas the second console.log logs 10 by capturing the count variable from outerscope.

========== Id ==========  
505

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#505-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
