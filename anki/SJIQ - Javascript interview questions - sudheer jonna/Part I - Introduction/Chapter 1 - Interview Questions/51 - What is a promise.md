========== Question ==========  

### What is a promise  

========== Answer ==========  

A promise is an object that may produce a single value some time in the future with either a resolved value or a reason that it’s not resolved(for example, network error). It will be in one of the 3 possible states: fulfilled, rejected, or pending.

The syntax of Promise creation looks like below,

```javascript
const promise = new Promise(function (resolve, reject) {
    // promise description
});
```

The usage of a promise would be as below,

```javascript
const promise = new Promise(
    (resolve) => {
        setTimeout(() => {
            resolve("I'm a Promise!");
        }, 5000);
    },
    (reject) => {},
);

promise.then((value) => console.log(value));
```

The action flow of a promise will be as below,

![promises](../../../../images/promises.png)

========== Id ==========  
51

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#51-What-is-a-promise

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
