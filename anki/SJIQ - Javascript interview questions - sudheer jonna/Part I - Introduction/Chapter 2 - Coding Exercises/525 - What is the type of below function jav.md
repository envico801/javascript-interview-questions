========== Question ==========  

### What is the type of below function?

```javascript
function add(a, b) {
    console.log('The input arguments are: ', a, b);
    return a + b;
}
```

-   1: Pure function

-   2: Impure function  

========== Answer ==========  

Answer: 2

Eventhough the above function returns the same result for the same arguments(input) that are passed in the function, the `console.log()` statement causes a function to have side effects because it affects the state of an external code. i.e, the `console` object's state and depends on it to perform the job. Hence, the above function considered as impure function.

========== Id ==========  
525

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#525-What-is-the-type-of-below-function-jav

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
