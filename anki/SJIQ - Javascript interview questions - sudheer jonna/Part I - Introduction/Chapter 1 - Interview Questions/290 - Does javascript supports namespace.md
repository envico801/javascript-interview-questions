==================== Question ====================  

### Does JavaScript supports namespace  

==================== Answer ====================  

JavaScript doesn’t support namespace by default. So if you create any
element(function, method, object, variable) then it becomes global and pollutes
the global namespace. Let's take an example of defining two functions without
any namespace,

```javascript
function func1() {
  console.log('This is a first definition');
}
function func1() {
  console.log('This is a second definition');
}
func1(); // This is a second definition
```

It always calls the second function definition. In this case, namespace will
solve the name collision problem.

==================== Id ====================  
290
<!--ID: 1707879827653-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#290-Does-javascript-supports-namespace

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
