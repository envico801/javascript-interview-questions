Q: How do you display data in a tabular format using console object  
A: The `console.table()` is used to display data in the console in a tabular format to visualize complex arrays or objects.
```js
const users = [
  { name: "John", id: 1, city: "Delhi" },
  { name: "Max", id: 2, city: "London" },
  { name: "Rod", id: 3, city: "Paris" },
];
console.table(users);
```
The data visualized in a table format,
![console-table](../../../../images/console-table.png)
**Not:** Remember that `console.table()` is not supported in IE.
<!--ID: 1693596688690-->

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