==================== Question ====================  

### How do you manipulate DOM using a service worker  

==================== Answer ====================  

Service worker can't access the DOM directly. But it can communicate with the
pages it controls by responding to messages sent via the `postMessage`
interface, and those pages can manipulate the DOM.

==================== Id ====================  
32

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#32-How-do-you-manipulate-dom-using-a-service

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
