========== Question ==========  

### What is the output of below code

```javascript
function foo() {
    let x = (y = 0);
    x++;
    y++;
    return x;
}
console.log(foo(), typeof x, typeof y);
```

-   1: 1, undefined and undefined

-   2: ReferenceError: X is not defined

-   3: 1, undefined and number

-   4: 1, number and number  

========== Answer ==========  

Answer: 3

Of course the return value of `foo()` is 1 due to the increment operator. But the statement `let x = y = 0` declares a local variable x. Whereas y declared as a global variable accidentally. This statement is equivalent to,

```javascript
let x;
window.y = 0;
x = window.y;
```

Since the block scoped variable x is undefined outside of the function, the type will be undefined too. Whereas the global variable `y` is available outside the function, the value is 0 and type is number.

========== Id ==========  
451

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#451-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
