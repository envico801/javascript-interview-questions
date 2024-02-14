==================== Question ====================  

### What are dynamic imports  

==================== Answer ====================  

The dynamic imports using `import()` function syntax allows us to load modules
on demand by using promises or the async/await syntax. Currently this feature is
in [stage4 proposal](https://github.com/tc39/proposal-dynamic-import). The main
advantage of dynamic imports is reduction of our bundle's sizes, the
size/payload response of our requests and overall improvements in the user
experience.  
The syntax of dynamic imports would be as below,

```javascript
import('./Module').then((Module) => Module.method());
```

==================== Id ====================  
318
<!--ID: 1707879825502-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#318-What-are-dynamic-imports

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
