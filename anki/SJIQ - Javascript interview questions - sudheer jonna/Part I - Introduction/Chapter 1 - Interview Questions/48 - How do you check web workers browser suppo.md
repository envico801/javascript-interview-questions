==================== Question ====================  

### How do you check web workers browser support  

==================== Answer ====================  

You need to check browser support for web workers before using it

```javascript
if (typeof Worker !== 'undefined') {
  // code for Web worker support.
} else {
  // Sorry! No Web Worker support..
}
```

==================== Id ====================  
48
<!--ID: 1707879843275-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#48-How-do-you-check-web-workers-browser-suppo

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
