==================== Question ====================  

### How do you display data in a tabular format using console object  

==================== Answer ====================  

The `console.table()` is used to display data in the console in a tabular format
to visualize complex arrays or objects.

```js
const users = [
  { name: 'John', id: 1, city: 'Delhi' },
  { name: 'Max', id: 2, city: 'London' },
  { name: 'Rod', id: 3, city: 'Paris' },
];
console.table(users);
```

The data visualized in a table format,  
![console-table](../../../../images/console-table.png)  
**Not:** Remember that `console.table()` is not supported in IE.

==================== Id ====================  
372

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#372-How-do-you-display-data-in-a-tabular-forma

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
