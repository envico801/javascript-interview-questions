Q: How do you verify that an argument is a Number or not  
A: The combination of IsNaN and isFinite methods are used to confirm whether an argument is a number or not.
```javascript
function isNumber(n) {
  return !isNaN(parseFloat(n)) && isFinite(n);
}
```
<!--ID: 1693596688595-->

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