Q: What is the easiest multi condition checking  
A: You can use `indexOf` to compare input with multiple values instead of checking each value as one condition.
```javascript
// Verbose approach
if (input === "first" || input === 1 || input === "second" || input === 2) {
  someFunction();
}
// Shortcut
if (["first", 1, "second", 2].indexOf(input) !== -1) {
  someFunction();
}
```
<!--ID: 1693596688224-->

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