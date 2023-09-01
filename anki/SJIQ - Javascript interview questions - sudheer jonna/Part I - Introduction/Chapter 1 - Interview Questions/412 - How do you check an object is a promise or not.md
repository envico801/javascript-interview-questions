Q: How do you check an object is a promise or not  
A: If you don't know if a value is a promise or not, wrapping the value as `Promise.resolve(value)` which returns a promise
```javascript
function isPromise(object) {
  if (Promise && Promise.resolve) {
    return Promise.resolve(object) == object;
  } else {
    throw "Promise not supported in your environment";
  }
}
var i = 1;
var promise = new Promise(function (resolve, reject) {
  resolve();
});
console.log(isPromise(i)); // false
console.log(isPromise(promise)); // true
```
Another way is to check for `.then()` handler type
```javascript
function isPromise(value) {
  return Boolean(value && typeof value.then === "function");
}
var i = 1;
var promise = new Promise(function (resolve, reject) {
  resolve();
});
console.log(isPromise(i)); // false
console.log(isPromise(promise)); // true
```
<!--ID: 1693596684700-->

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