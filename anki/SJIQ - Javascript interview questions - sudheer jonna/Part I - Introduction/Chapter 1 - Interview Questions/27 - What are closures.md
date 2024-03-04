========== Question ==========  

### What are closures  

========== Answer ==========  

A closure is the combination of a function and the lexical environment within
which that function was declared. i.e, It is an inner function that has access
to the outer or enclosing function’s variables, functions and other data even
after the outer function has finished its execution. The closure has three scope
chains.

1. Own scope where variables defined between its curly brackets

2. Outer function’s variables

3. Global variables

Let's take an example of closure concept,

```javascript
function Welcome(name) {
  var greetingInfo = function (message) {
     console.log(message + ' ' + name);
  };
  return greetingInfo;
}
var myFunction = Welcome('John');
myFunction('Welcome '); //Output: Welcome John
myFunction('Hello Mr.'); //output: Hello Mr. John
```

As per the above code, the inner function(i.e, greetingInfo) has access to the
variables in the outer function scope(i.e, Welcome) even after the outer
function has returned.

========== Id ==========  
27

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#27-What-are-closures

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
