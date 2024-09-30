========== Question ==========  

### What is the output of below code?

```javascript
getMessage();
var getMessage = () => {
    console.log('Good morning');
};
```

-   1: Good morning

-   2: getMessage is not a function

-   3: getMessage is not defined

-   4: Undefined  

========== Answer ==========  

Answer: 2

Hoisting will move variables and functions to be the top of scope. Even though getMessage is an arrow function the above function will considered as a varible due to it's variable declaration or assignment. So the variables will have undefined value in memory phase and throws an error '`getMessage` is not a function' at the code execution phase.

========== Id ==========  
508

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#508-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
