==================== Question ====================  

### What is the output of below code

```javascript
function outer(f = inner()) {
  function inner() {
    return 'Inner';
  }
}
outer();
```

- 1: ReferenceError
- 2: Inner  

==================== Answer ====================  

Answer: 1  
The functions and variables declared in the function body cannot be referred
from default value parameter initializers. If you still try to access, it throws
a run-time ReferenceError(i.e, `inner` is not defined).

==================== Id ====================  
490

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#490-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
