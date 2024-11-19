========== Question ==========  

### What is the output of below for loops

```javascript
for (var i = 0; i < 4; i++) {
    // global scope
    setTimeout(() => console.log(i));
}

for (let i = 0; i < 4; i++) {
    // block scope
    setTimeout(() => console.log(i));
}
```  

========== Answer ==========  

The output of the above for loops is 4 4 4 4 and 0 1 2 3

**Explanation:** Due to the event queue/loop of javascript, the `setTimeout` callback function is called after the loop has been executed. Since the variable i is declared with the `var` keyword it became a global variable and the value was equal to 4 using iteration when the time `setTimeout` function is invoked. Hence, the output of the first loop is `4 4 4 4`.

Whereas in the second loop, the variable i is declared as the `let` keyword it becomes a block scoped variable and it holds a new value(0, 1 ,2 3) for each iteration. Hence, the output of the first loop is `0 1 2 3`.

========== Id ==========  
303

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#303-What-is-the-output-of-below-for-loops-j

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
