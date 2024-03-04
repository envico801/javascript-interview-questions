========== Question ==========  

### What is global execution context?  

========== Answer ==========  

The global execution context is the default or first execution context that is
created by the JavaScript engine before any code is executed(i.e, when the file
first loads in the browser). All the global code that is not inside a function
or object will be executed inside this global execution context. Since JS engine
is single threaded there will be only one global environment and there will be
only one global execution context.

For example, the below code other than code inside any function or object is
executed inside the global execution context.

```javascript
var x = 10;
function A() {
  console.log('Start function A');
  function B() {
     console.log('In function B');
  }
  B();
}
A();
console.log('GlobalContext');
```

========== Id ==========  
432

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#432-What-is-global-execution-context

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
