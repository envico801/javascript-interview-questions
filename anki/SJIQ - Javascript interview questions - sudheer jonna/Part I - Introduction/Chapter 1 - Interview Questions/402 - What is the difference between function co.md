==================== Question ====================  

### What is the difference between Function constructor and function declaration  

==================== Answer ====================  

The functions which are created with `Function constructor` do not create
closures to their creation contexts but they are always created in the global
scope. i.e, the function can access its own local variables and global scope
variables only. Whereas function declarations can access outer function
variables(closures) too.  
Let's see this difference with an example,  
**Function Constructor:**

```javascript
var a = 100;
function createFunction() {
  var a = 200;
  return new Function('return a;');
}
console.log(createFunction()()); // 100
```

**Function declaration:**

```javascript
var a = 100;
function createFunction() {
  var a = 200;
  return function func() {
    return a;
  };
}
console.log(createFunction()()); // 200
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#402-What-is-the-difference-between-function-co

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
