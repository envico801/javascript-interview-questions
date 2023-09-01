Q: How do you access history in javascript  
A: The window.history object contains the browser's history. You can load previous and next URLs in the history using back() and next() methods.
```javascript
function goBack() {
  window.history.back();
}
function goForward() {
  window.history.forward();
}
```
**Note:** You can also access history without window prefix.
<!--ID: 1693596716090-->

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