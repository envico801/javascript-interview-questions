========== Question ==========  

### What are the possible side-effects in javascript?  

========== Answer ==========  

A side effect is the modification of the state through the invocation of a function or expression. These side effects make our function impure by default. Below are some side effects which make function impure,

-   Making an HTTP request. Asynchronous functions such as fetch and promise are impure.

-   DOM manipulations

-   Mutating the input data

-   Printing to a screen or console: For example, console.log() and alert()

-   Fetching the current time

-   Math.random() calls: Modifies the internal state of Math object

========== Id ==========  
444

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#444-What-are-the-possible-side-effects-in-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
