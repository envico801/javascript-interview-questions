==================== Question ====================  

### What is the output of below code

```javascript
async function func() {
  return 10;
}
console.log(func());
```

- 1: Promise {\<fulfilled\>: 10}
- 2: 10
- 3: SyntaxError
- 4: Promise {\<rejected\>: 10}  

==================== Answer ====================  

Answer: 1  
Async functions always return a promise. But even if the return value of an
async function is not explicitly a promise, it will be implicitly wrapped in a
promise. The above async function is equivalent to below expression,

```javascript
function func() {
  return Promise.resolve(10);
}
```

==================== Id ====================  
473
<!--ID: 1707879787971-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#473-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
