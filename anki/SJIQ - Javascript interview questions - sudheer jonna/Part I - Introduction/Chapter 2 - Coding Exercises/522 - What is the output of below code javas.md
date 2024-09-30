========== Question ==========  

### What is the output of below code?

```javascript
let user1 = {
    name: 'Jacob',
    age: 28,
};
let user2 = {
    name: 'Jacob',
    age: 28,
};
console.log(user1 === user2);
```

-   1: True

-   2: False

-   3: Compile time error  

========== Answer ==========  

Answer: 2

In JavaScript, the variables such as objects, arrays and functions comes under pass by reference. When you try to compare two objects with same content, it is going to compare memory address or reference of those variables. These variables always create separate memory blocks hence the comparison is always going to return false value.

========== Id ==========  
522

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#522-What-is-the-output-of-below-code-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
