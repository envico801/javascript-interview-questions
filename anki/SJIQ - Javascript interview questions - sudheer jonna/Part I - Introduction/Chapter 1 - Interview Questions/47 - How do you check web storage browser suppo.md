==================== Question ====================  

### How do you check web storage browser support  

==================== Answer ====================  

You need to check browser support for localStorage and sessionStorage before
using web storage,

```javascript
if (typeof Storage !== 'undefined') {
  // Code for localStorage/sessionStorage.
} else {
  // Sorry! No Web Storage support..
}
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#47-How-do-you-check-web-storage-browser-suppo

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
