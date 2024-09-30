========== Question ==========  

### What is the output of below code

```javascript
let [a, ...b] = [1, 2, 3, 4, 5];
console.log(a, b);
```

-   1: 1, [2, 3, 4, 5]

-   2: 1, {2, 3, 4, 5}

-   3: SyntaxError

-   4: 1, [2, 3, 4]  

========== Answer ==========  

Answer: 3

When using rest parameters, trailing commas are not allowed and will throw a SyntaxError.

If you remove the trailing comma then it displays 1st answer

```javascript
let [a, ...b] = [1, 2, 3, 4, 5];
console.log(a, b); // 1, [2, 3, 4, 5]
```

========== Id ==========  
472

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#472-What-is-the-output-of-below-code-javasc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
