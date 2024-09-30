========== Question ==========  

### What is microtask  

========== Answer ==========  

Microtask is the javascript code which needs to be executed immediately after the currently executing task/microtask is completed. They are kind of blocking in nature. i.e, The main thread will be blocked until the microtask queue is empty.

The main sources of microtasks are Promise.resolve, Promise.reject, MutationObservers, IntersectionObservers etc

**Note:** All of these microtasks are processed in the same turn of the event loop.

========== Id ==========  
388

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#388-What-is-microtask

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
