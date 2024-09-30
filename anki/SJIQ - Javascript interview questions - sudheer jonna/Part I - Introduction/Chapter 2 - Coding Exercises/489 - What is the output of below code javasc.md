========== Question ==========  

### What is the output of below code

```javascript
function greet(greeting, name, message = greeting + ' ' + name) {
    console.log([greeting, name, message]);
}
greet('Hello', 'John');
greet('Hello', 'John', 'Good morning!');
```

-   1: SyntaxError

-   2: ['Hello', 'John', 'Hello John'], ['Hello', 'John', 'Good morning!']  

========== Answer ==========  

Answer: 2

Since parameters defined earlier are available to later default parameters, this code snippet doesn't throw any error.

========== Id ==========  
489

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#489-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
