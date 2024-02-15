==================== Question ====================  

### How do you reuse information across service worker restarts  

==================== Answer ====================  

The problem with service worker is that it gets terminated when not in use, and
restarted when it's next needed, so you cannot rely on global state within a
service worker's `onfetch` and `onmessage` handlers. In this case, service
workers will have access to IndexedDB API in order to persist and reuse across
restarts.

==================== Id ====================  
33
<!--ID: 1707879890663-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#33-How-do-you-reuse-information-across-servic

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
