========== Question ==========  

### What is the output of below code

```javascript
function* yieldAndReturn() {
    yield 1;
    return 2;
    yield 3;
}

var myGenObj = yieldAndReturn();
console.log(myGenObj.next());
console.log(myGenObj.next());
console.log(myGenObj.next());
```

-   1: { value: 1, done: false }, { value: 2, done: true }, { value: undefined, done: true }

-   2: { value: 1, done: false }, { value: 2, done: false }, { value: undefined, done: true }

-   3: { value: 1, done: false }, { value: 2, done: true }, { value: 3, done: true }

-   4: { value: 1, done: false }, { value: 2, done: false }, { value: 3, done: true }  

========== Answer ==========  

Answer: 1

A return statement in a generator function will make the generator finish. If a value is returned, it will be set as the value property of the object and done property to true. When a generator is finished, subsequent next() calls return an object of this form: `{value: undefined, done: true}`.

========== Id ==========  
494

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#494-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
