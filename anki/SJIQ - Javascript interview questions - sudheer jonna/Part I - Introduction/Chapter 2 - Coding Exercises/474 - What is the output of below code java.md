==================== Question ====================  

### What is the output of below code

```javascript
async function func() {
  await 10;
}
console.log(func());
```

- 1: Promise {\<fulfilled\>: 10}
- 2: 10
- 3: SyntaxError
- 4: Promise {\<resolved\>: undefined}  

==================== Answer ====================  

Answer: 4  
The await expression returns value 10 with promise resolution and the code after
each await expression can be treated as existing in a `.then` callback. In this
case, there is no return expression at the end of the function. Hence, the
default return value of `undefined` is returned as the resolution of the
promise. The above async function is equivalent to below expression,

```javascript
function func() {
  return Promise.resolve(10).then(() => undefined);
}
```

==================== Id ====================  
474

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#474-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
