Q: What is a spread operator  
A: Spread operator allows iterables( arrays / objects / strings ) to be expanded into single arguments/elements. Let's take an example to see this behavior,
```javascript
function calculateSum(x, y, z) {
  return x + y + z;
}
const numbers = [1, 2, 3];
console.log(calculateSum(...numbers)); // 6
```
<!--ID: 1693596706402-->

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