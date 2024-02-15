==================== Question ====================  

### What happens if you do not use rest parameter as a last argument  

==================== Answer ====================  

The rest parameter should be the last argument, as its job is to collect all the
remaining arguments into an array. For example, if you define a function like
below it doesn’t make any sense and will throw an error.

```javascript
     function someFunc(a,…b,c){
     //You code goes here
     return;
     }
```

==================== Id ====================  
186
<!--ID: 1707879850405-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#186-What-happens-if-you-do-not-use-rest-parame

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
