==================== Question ====================  

### What is the output of below code

```javascript
try {
  setTimeout(() => {
    console.log('try block');
    throw new Error(`An exception is thrown`);
  }, 1000);
} catch (err) {
  console.log('Error: ', err);
}
```

- 1: try block, Error: An exception is thrown
- 2: Error: An exception is thrown
- 3: try block, Uncaught Error: Exception is thrown
- 4: Uncaught Error: Exception is thrown  

==================== Answer ====================  

Answer: 3  
If you put `setTimeout` and `setInterval` methods inside the try clause and an
exception is thrown, the catch clause will not catch any of them. This is
because the try...catch statement works synchronously, and the function in the
above code is executed asynchronously after a certain period of time. Hence, you
will see runtime exception without catching the error. To resolve this issue,
you have to put the try...catch block inside the function as below,

```javascript
setTimeout(() => {
  try {
    console.log('try block');
    throw new Error(`An exception is thrown`);
  } catch (err) {
    console.log('Error: ', err);
  }
}, 1000);
```

You can use `.catch()` function in promises to avoid these issues with
asynchronous code.

==================== Id ====================  
527

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#527-What-is-the-output-of-below-code-jav

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
