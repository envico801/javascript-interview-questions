==================== Question ====================  

### How do you check browser support for server-sent events  

==================== Answer ====================  

You can perform browser support for server-sent events before using it as below,

```javascript
if (typeof EventSource !== 'undefined') {
  // Server-sent events supported. Let's have some code here!
} else {
  // No server-sent events supported
}
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#59-How-do-you-check-browser-support-for-serve

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
