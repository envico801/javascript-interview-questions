========== Question ==========  

### What is the output of below code

```javascript
const USER = { age: 30 };
USER.age = 25;
console.log(USER.age);
```

-   1: 30

-   2: 25

-   3: Uncaught TypeError

-   4: SyntaxError  

========== Answer ==========  

Answer: 2

Even though we used constant variables, the content of it is an object and the object's contents (e.g properties) can be altered. Hence, the change is going to be valid in this case.

========== Id ==========  
500

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#500-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
