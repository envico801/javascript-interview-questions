==================== Question ====================  

### How do get query string values in javascript  

==================== Answer ====================  

You can use URLSearchParams to get query string values in javascript. Let's see
an example to get the client code value from URL query string,

```javascript
const urlParams = new URLSearchParams(window.location.search);
const clientCode = urlParams.get('clientCode');
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#124-How-do-get-query-string-values-in-javascri

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
