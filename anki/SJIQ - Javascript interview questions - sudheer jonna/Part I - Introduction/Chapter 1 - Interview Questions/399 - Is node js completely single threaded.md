==================== Question ====================  

### Is Node.js completely single threaded  

==================== Answer ====================  

Node is a single thread, but some of the functions included in the Node.js
standard library(e.g, fs module functions) are not single threaded. i.e, Their
logic runs outside of the Node.js single thread to improve the speed and
performance of a program.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#399-Is-node-js-completely-single-threaded

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
