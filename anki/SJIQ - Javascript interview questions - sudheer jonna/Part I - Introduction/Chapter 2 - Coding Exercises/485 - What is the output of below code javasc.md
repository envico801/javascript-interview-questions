========== Question ==========  

### What is the output of below code

```javascript
function area({ length = 10, width = 20 }) {
  console.log(length * width);
}
area();
```

- 1: 200

- 2: Error

- 3: undefined

- 4: 0  

========== Answer ==========  

Answer: 2

If you leave out the right-hand side assignment for the destructuring object,
the function will look for at least one argument to be supplied when invoked.
Otherwise you will receive an error
`Error: Cannot read property 'length' of undefined` as mentioned above.

You can avoid the error with either of the below changes,

1. **Pass at least an empty object:**

```javascript
function area({ length = 10, width = 20 }) {
  console.log(length * width);
}
area({});
```

2. **Assign default empty object:**

```javascript
function area({ length = 10, width = 20 } = {}) {
  console.log(length * width);
}
area();
```

========== Id ==========  
485

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#485-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
