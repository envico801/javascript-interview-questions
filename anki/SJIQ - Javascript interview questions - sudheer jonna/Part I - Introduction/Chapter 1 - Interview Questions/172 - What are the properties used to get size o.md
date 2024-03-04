========== Question ==========  

### What are the properties used to get size of window  

========== Answer ==========  

You can use innerWidth, innerHeight, clientWidth, clientHeight properties of
windows, document element and document body objects to find the size of a
window. Let's use them combination of these properties to calculate the size of
a window or document,

```javascript
var width =
  window.innerWidth ||
  document.documentElement.clientWidth ||
  document.body.clientWidth;
var height =
  window.innerHeight ||
  document.documentElement.clientHeight ||
  document.body.clientHeight;
```

========== Id ==========  
172

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#172-What-are-the-properties-used-to-get-size-o

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
