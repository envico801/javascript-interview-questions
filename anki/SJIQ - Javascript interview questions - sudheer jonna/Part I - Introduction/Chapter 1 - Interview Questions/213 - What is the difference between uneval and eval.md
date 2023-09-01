Q: What is the difference between uneval and eval  
A: The `uneval` function returns the source of a given object; whereas the `eval` function does the opposite, by evaluating that source code in a different memory area. Let's see an example to clarify the difference,
```javascript
var msg = uneval(function greeting() {
  return "Hello, Good morning";
});
var greeting = eval(msg);
greeting(); // returns "Hello, Good morning"
```
<!--ID: 1693596703787-->

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