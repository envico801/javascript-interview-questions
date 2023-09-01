Q: What is the purpose of EvalError object  
A: The EvalError object indicates an error regarding the global `eval()` function. Even though this exception is not thrown by JavaScript anymore, the EvalError object remains for compatibility. The syntax of this expression would be as below,
```javascript
new EvalError([message[, fileName[, lineNumber]]])
```
You can throw EvalError with in try...catch block as below,
```javascript
try {
throw new EvalError('Eval function error', 'someFile.js', 100);
} catch (e) {
console.log(e.message, e.name, e.fileName);              // "Eval function error", "EvalError", "someFile.js"
```
<!--ID: 1693596691757-->

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