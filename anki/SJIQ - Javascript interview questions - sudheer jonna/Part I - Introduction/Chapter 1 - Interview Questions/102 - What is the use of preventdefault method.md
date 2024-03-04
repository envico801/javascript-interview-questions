========== Question ==========  

### What is the use of preventDefault method  

========== Answer ==========  

The preventDefault() method cancels the event if it is cancelable, meaning that
the default action or behaviour that belongs to the event will not occur. For
example, prevent form submission when clicking on submit button and prevent
opening the page URL when clicking on hyperlink are some common use cases.

```javascript
document.getElementById('link').addEventListener('click', function (event) {
  event.preventDefault();
});
```

**Note:** Remember that not all events are cancelable.

========== Id ==========  
102

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#102-What-is-the-use-of-preventdefault-method

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
