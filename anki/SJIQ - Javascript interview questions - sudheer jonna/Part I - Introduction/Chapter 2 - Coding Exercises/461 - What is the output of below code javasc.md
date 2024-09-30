========== Question ==========  

### What is the output of below code

```javascript
const printNumbersArrow = (first, second, first) => {
    console.log(first, second, first);
};
printNumbersArrow(1, 2, 3);
```

-   1: 1, 2, 3

-   2: 3, 2, 3

-   3: SyntaxError: Duplicate parameter name not allowed in this context

-   4: 1, 2, 1  

========== Answer ==========  

Answer: 3

Unlike regular functions, the arrow functions doesn't not allow duplicate parameters in either strict or non-strict mode. So you can see `SyntaxError` in the console.

========== Id ==========  
461

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#461-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
