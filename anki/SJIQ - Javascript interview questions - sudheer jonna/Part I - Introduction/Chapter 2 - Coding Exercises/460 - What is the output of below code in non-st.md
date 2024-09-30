========== Question ==========  

### What is the output of below code in non-strict mode

```javascript
function printNumbers(first, second, first) {
    console.log(first, second, first);
}
printNumbers(1, 2, 3);
```

-   1: 1, 2, 3

-   2: 3, 2, 3

-   3: SyntaxError: Duplicate parameter name not allowed in this context

-   4: 1, 2, 1  

========== Answer ==========  

Answer: 2

In non-strict mode, the regular JavaScript functions allow duplicate named parameters. The above code snippet has duplicate parameters on 1st and 3rd parameters.

The value of the first parameter is mapped to the third argument which is passed to the function. Hence, the 3rd argument overrides the first parameter.

**Note:** In strict mode, duplicate parameters will throw a Syntax Error.

========== Id ==========  
460

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#460-What-is-the-output-of-below-code-in-non-st

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
