========== Question ==========  

### What is a higher order function  

========== Answer ==========  

A higher-order function is a function that accepts another function as an
argument or returns a function as a return value or both.

```javascript
const firstOrderFunc = () => console.log('Hello, I am a First order function');
const higherOrder = (ReturnFirstOrderFunc) => ReturnFirstOrderFunc();
higherOrder(firstOrderFunc);
```

========== Id ==========  
13

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#13-What-is-a-higher-order-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
