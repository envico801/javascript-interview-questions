==================== Question ====================  

### What is an IIFE (Immediately Invoked Function Expression)  

==================== Answer ====================  

IIFE (Immediately Invoked Function Expression) is a JavaScript function that
runs as soon as it is defined. The signature of it would be as below,

```javascript
(function () {
  // logic here
})();
```

The primary reason to use an IIFE is to obtain data privacy because any
variables declared within the IIFE cannot be accessed by the outside world. i.e,
If you try to access variables from the IIFE then it throws an error as below,

```javascript
(function () {
  var message = 'IIFE';
  console.log(message);
})();
console.log(message); //Error: message is not defined
```

==================== Id ====================  
22
<!--ID: 1707879815446-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#22-What-is-an-iife-immediately-invoked-funct

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
