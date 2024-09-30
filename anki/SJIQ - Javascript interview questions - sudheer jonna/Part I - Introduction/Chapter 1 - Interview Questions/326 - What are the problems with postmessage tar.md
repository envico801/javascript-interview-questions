========== Question ==========  

### What are the problems with postmessage target origin as wildcard  

========== Answer ==========  

The second argument of postMessage method specifies which origin is allowed to receive the message. If you use the wildcard “\*” as an argument then any origin is allowed to receive the message. In this case, there is no way for the sender window to know if the target window is at the target origin when sending the message. If the target window has been navigated to another origin, the other origin would receive the data. Hence, this may lead to XSS vulnerabilities.

```javascript
targetWindow.postMessage(message, '*');
```

========== Id ==========  
326

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#326-What-are-the-problems-with-postmessage-tar

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
