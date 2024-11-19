========== Question ==========  

### What is the output of below code

```javascript
function delay() {
    return new Promise((resolve) => setTimeout(resolve, 2000));
}

async function delayedLog(item) {
    await delay();
    console.log(item);
}

async function process(array) {
    array.forEach(async (item) => {
        await delayedLog(item);
    });
    console.log('Process completed!');
}
process([1, 2, 3, 5]);
```

-   1: 1 2 3 5 and Process completed!

-   2: 5 5 5 5 and Process completed!

-   3: Process completed! and 5 5 5 5

-   4: Process completed! and 1 2 3 5  

========== Answer ==========  

Answer: 4

The forEach method will not wait until all items are finished but it just runs the tasks and goes next. Hence, the last statement is displayed first followed by a sequence of promise resolutions.

But you control the array sequence using for..of loop,

```javascript
async function processArray(array) {
    for (const item of array) {
        await delayedLog(item);
    }
    console.log('Process completed!');
}
```

========== Id ==========  
476

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#476-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
