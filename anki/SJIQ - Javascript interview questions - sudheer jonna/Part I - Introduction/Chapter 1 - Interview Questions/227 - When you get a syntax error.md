Q: When you get a syntax error  
A: A SyntaxError is thrown if you try to evaluate code with a syntax error. For example, the below missing quote for the function parameter throws a syntax error
```javascript
try {
  eval("greeting('welcome)"); // Missing ' will produce an error
} catch (err) {
  console.log(err.name);
}
```
<!--ID: 1693596702484-->

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