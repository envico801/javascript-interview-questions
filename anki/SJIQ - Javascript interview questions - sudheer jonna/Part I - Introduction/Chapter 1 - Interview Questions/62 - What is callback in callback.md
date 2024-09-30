========== Question ==========  

### What is callback in callback  

========== Answer ==========  

You can nest one callback inside in another callback to execute the actions sequentially one by one. This is known as callbacks in callbacks.

```javascript
loadScript('/script1.js', function (script) {
    console.log('first script is loaded');
    loadScript('/script2.js', function (script) {
        console.log('second script is loaded');
        loadScript('/script3.js', function (script) {
            console.log('third script is loaded');
            // after all scripts are loaded
        });
    });
});
```

========== Id ==========  
62

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#62-What-is-callback-in-callback

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
