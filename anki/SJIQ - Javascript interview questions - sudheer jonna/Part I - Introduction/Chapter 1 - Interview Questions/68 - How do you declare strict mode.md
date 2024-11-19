========== Question ==========  

### How do you declare strict mode  

========== Answer ==========  

The strict mode is declared by adding "use strict"; to the beginning of a script or a function.

If declared at the beginning of a script, it has global scope.

```javascript
'use strict';
x = 3.14; // This will cause an error because x is not declared
```

and if you declare inside a function, it has local scope

```javascript
x = 3.14; // This will not cause an error.
myFunction();

function myFunction() {
    'use strict';
    y = 3.14; // This will cause an error
}
```

========== Id ==========  
68

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#68-How-do-you-declare-strict-mode

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
