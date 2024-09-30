========== Question ==========  

### What is the output of below code?

```javascript
message();
function message() {
    console.log('Hello');
}
function message() {
    console.log('Bye');
}
```

-   1: Reference error: message is not defined

-   2: Hello

-   3: Bye

-   4: Compile time error  

========== Answer ==========  

Answer: 3

As part of hoisting, initially JavaScript Engine or compiler will store first function in heap memory but later rewrite or replaces with redefined function content.

========== Id ==========  
516

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#516-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
