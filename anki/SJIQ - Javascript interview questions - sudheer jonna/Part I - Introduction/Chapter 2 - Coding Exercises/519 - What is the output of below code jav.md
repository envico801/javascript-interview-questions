==================== Question ====================  

### What is the output of below code

```javascript
var expressionOne = function functionOne() {
  console.log('functionOne');
};
functionOne();
```

- 1: functionOne is not defined
- 2: functionOne
- 3: console.log("functionOne")
- 4: undefined  

==================== Answer ====================  

Answer: 1  
The function call `functionOne` is not going to be part of scope chain and it
has it's own execution context with the enclosed variable environment. i.e, It
won't be accessed from global context. Hence, there will be an error while
invoking the function as `functionOne is not defined`.

==================== Id ====================  
519
<!--ID: 1707879793670-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#519-What-is-the-output-of-below-code-jav

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
