Q: How do you capture browser back button  
A: The `window.onbeforeunload` method is used to capture browser back button events. This is helpful to warn users about losing the current data.
```javascript
window.onbeforeunload = function () {
  alert("You work will be lost");
};
```
<!--ID: 1693596688124-->

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