========== Question ==========  

### What is a rest parameter  

========== Answer ==========  

Rest parameter is an improved way to handle function parameters which allows us to represent an indefinite number of arguments as an array. The syntax would be as below,

```javascript
function f(a, b, ...theArgs) {
    // ...
}
```

For example, let's take a sum example to calculate on dynamic number of parameters,

```javascript
function sum(...args) {
    let total = 0;
    for (const i of args) {
        total += i;
    }
    return total;
}

console.log(sum(1, 2)); //3
console.log(sum(1, 2, 3)); //6
console.log(sum(1, 2, 3, 4)); //13
console.log(sum(1, 2, 3, 4, 5)); //15
```

**Note:** Rest parameter is added in ES2015 or ES6

========== Id ==========  
185

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#185-What-is-a-rest-parameter

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
