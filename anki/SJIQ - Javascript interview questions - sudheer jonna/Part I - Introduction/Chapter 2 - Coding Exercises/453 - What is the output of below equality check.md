========== Question ==========  

### What is the output of below equality check

```javascript
console.log(0.1 + 0.2 === 0.3);
```

- 1: false

- 2: true  

========== Answer ==========  

Answer: 1

This is due to the float point math problem. Since the floating point numbers
are encoded in binary format, the addition operations on them lead to rounding
errors. Hence, the comparison of floating points doesn't give expected results.

You can find more details about the explanation here
[0.30000000000000004.com/](https://0.30000000000000004.com/)

========== Id ==========  
453

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#453-What-is-the-output-of-below-equality-check

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
