========== Question ==========  

### What is the output of below code

```javascript
function delay() {
return new Promise(resolve => setTimeout(resolve, 2000));
}
async function delayedLog(item) {
await delay();
console.log(item);
}
async function processArray(array) {
array.forEach(item => {
 await delayedLog(item);
})
}
processArray([1, 2, 3, 4]);
```

- 1: SyntaxError

- 2: 1, 2, 3, 4

- 3: 4, 4, 4, 4

- 4: 4, 3, 2, 1  

========== Answer ==========  

Answer: 1

Even though “processArray” is an async function, the anonymous function that we
use for `forEach` is synchronous. If you use await inside a synchronous function
then it throws a syntax error.

========== Id ==========  
475

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#475-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
