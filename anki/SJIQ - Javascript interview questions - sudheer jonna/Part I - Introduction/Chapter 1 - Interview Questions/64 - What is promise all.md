==================== Question ====================  

### What is promise.all  

==================== Answer ====================  

Promise.all is a promise that takes an array of promises as an input (an
iterable), and it gets resolved when all the promises get resolved or any one of
them gets rejected. For example, the syntax of promise.all method is below,

```javascript
Promise.all([Promise1, Promise2, Promise3]) .then(result) => {   console.log(result) }) .catch(error => console.log(`Error in promises ${error}`))
```

**Note:** Remember that the order of the promises(output the result) is
maintained as per input order.

==================== Id ====================  
64

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#64-What-is-promise-all

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
