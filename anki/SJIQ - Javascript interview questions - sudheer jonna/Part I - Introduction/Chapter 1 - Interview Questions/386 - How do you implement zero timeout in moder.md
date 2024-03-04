========== Question ==========  

### How do you implement zero timeout in modern browsers  

========== Answer ==========  

You can't use setTimeout(fn, 0) to execute the code immediately due to minimum
delay of greater than 0ms. But you can use window.postMessage() to achieve this
behavior.

========== Id ==========  
386

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#386-How-do-you-implement-zero-timeout-in-moder

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
