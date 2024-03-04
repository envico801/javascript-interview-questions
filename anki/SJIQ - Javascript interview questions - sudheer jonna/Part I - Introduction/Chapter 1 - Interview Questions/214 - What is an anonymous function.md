========== Question ==========  

### What is an anonymous function  

========== Answer ==========  

An anonymous function is a function without a name! Anonymous functions are
commonly assigned to a variable name or used as a callback function. The syntax
would be as below,

```javascript
function (optionalParameters) {
  //do something
}
const myFunction = function(){ //Anonymous function assigned to a variable
  //do something
};
[1, 2, 3].map(function(element){ //Anonymous function used as a callback function
  //do something
});
```

Let's see the above anonymous function in an example,

```javascript
var x = function (a, b) {
  return a * b;
};
var z = x(5, 10);
console.log(z); // 50
```

========== Id ==========  
214

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#214-What-is-an-anonymous-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
