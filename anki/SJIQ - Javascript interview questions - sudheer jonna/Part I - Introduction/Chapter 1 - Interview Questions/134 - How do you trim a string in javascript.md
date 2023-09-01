Q: How do you trim a string in javascript  
A: JavaScript provided a trim method on string types to trim any whitespaces present at the beginning or ending of the string.
```javascript
"  Hello World   ".trim(); //Hello World
```
If your browser(<IE9) doesn't support this method then you can use below polyfill.
```javascript
if (!String.prototype.trim) {
  (function () {
    // Make sure we trim BOM and NBSP
    var rtrim = /^[\s\uFEFF\xA0]+|[\s\uFEFF\xA0]+$/g;
    String.prototype.trim = function () {
      return this.replace(rtrim, "");
    };
  })();
}
```
<!--ID: 1693596711494-->

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