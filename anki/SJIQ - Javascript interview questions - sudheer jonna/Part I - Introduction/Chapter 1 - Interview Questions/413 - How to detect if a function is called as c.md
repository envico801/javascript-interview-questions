==================== Question ====================  

### How to detect if a function is called as constructor  

==================== Answer ====================  

You can use `new.target` pseudo-property to detect whether a function was called
as a constructor(using the new operator) or as a regular function call.

1. If a constructor or function invoked using the new operator, new.target
   returns a reference to the constructor or function.
2. For function calls, new.target is undefined.

```javascript
function Myfunc() {
  if (new.target) {
    console.log('called with new');
  } else {
    console.log('not called with new');
  }
}
new Myfunc(); // called with new
Myfunc(); // not called with new
Myfunc.call({}); // not called with new
```

==================== Id ====================  
413
<!--ID: 1707879819481-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#413-How-to-detect-if-a-function-is-called-as-c

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
