========== Question ==========  

### What is the output of below code?

```javascript
printHello();

printMessage();

function printHello() {
    console.log('Hello');

    function printMessage() {
        console.log('Good day');
    }
}
```

-   1: Hello, Good day

-   2: Reference Error: printHello is not defined, Reference Error: printMessage is not defined

-   3: Reference Error: printHello is not defined, Good day

-   4: Hello, Reference Error: printMessage is not defined  

========== Answer ==========  

Answer: 4

The function `printHello` is hoisted to the top of the global scope and prints "Hello" to the console. Even `printMessage` function is hoisted, but it is lifted to the local scope(in "printHello") it was declared in. That is the reason you will endup with reference error for second function call.

But if the second function is invoked in the first function itself, there won't be any reference error.

```javascript
printHello();

function printHello() {
    printMessage();
    console.log('Hello');

    function printMessage() {
        console.log('Good day');
    }
}
```

========== Id ==========  
531

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#531-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
