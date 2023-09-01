Q: What is the difference between let and var  
A: You can list out the differences in a tabular format

| var                                                   | let                         |
| ----------------------------------------------------- | --------------------------- |
| It is been available from the beginning of JavaScript | Introduced as part of ES6   |
| It has function scope                                 | It has block scope          |
| Variables will be hoisted                             | Hoisted but not initialized |
Let's take an example to see the difference,
```javascript
function userDetails(username) {
  if (username) {
    console.log(salary); // undefined due to hoisting
    console.log(age); // ReferenceError: Cannot access 'age' before initialization
    let age = 30;
    var salary = 10000;
  }
  console.log(salary); //10000 (accessible due to function scope)
  console.log(age); //error: age is not defined(due to block scope)
}
userDetails("John");
```
<!--ID: 1693596722001-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript #Interview

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store