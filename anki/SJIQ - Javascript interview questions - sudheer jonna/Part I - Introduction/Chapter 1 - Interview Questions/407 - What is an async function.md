========== Question ==========  

### What is an async function  

========== Answer ==========  

An async function is a function declared with the `async` keyword which enables asynchronous, promise-based behavior to be written in a cleaner style by avoiding promise chains. These functions can contain zero or more `await` expressions.

Let's take a below async function example,

```javascript
async function logger() {
    let data = await fetch('http://someapi.com/users'); // pause until fetch returns
    console.log(data);
}
logger();
```

It is basically syntax sugar over ES2015 promises and generators.

========== Id ==========  
407

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#407-What-is-an-async-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
