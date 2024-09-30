========== Question ==========  

### What is the output of below code

```javascript
console.log(1 < 2 < 3);
console.log(3 > 2 > 1);
```

-   1: true, true

-   2: true, false

-   3: SyntaxError, SyntaxError,

-   4: false, false  

========== Answer ==========  

Answer: 2

The important point is that if the statement contains the same operators(e.g, < or >) then it can be evaluated from left to right.

The first statement follows the below order,

1. console.log(1 < 2 < 3);

2. console.log(true < 3);

3. console.log(1 < 3); // True converted as `1` during comparison

4. True

Whereas the second statement follows the below order,

1. console.log(3 > 2 > 1);

2. console.log(true > 1);

3. console.log(1 > 1); // False converted as `0` during comparison

4. False

========== Id ==========  
459

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#459-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
