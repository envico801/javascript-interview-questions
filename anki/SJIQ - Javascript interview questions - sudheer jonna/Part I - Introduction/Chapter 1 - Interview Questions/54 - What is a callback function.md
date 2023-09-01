Q: What is a callback function  
A: A callback function is a function passed into another function as an argument. This function is invoked inside the outer function to complete an action.  
Let's take a simple example of how to use callback function
```javascript
function callbackFunction(name) {
  console.log("Hello " + name);
}
function outerFunction(callback) {
  let name = prompt("Please enter your name.");
  callback(name);
}
outerFunction(callbackFunction);
```
<!--ID: 1693596718312-->

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