========== Question ==========  

### What is the easiest way to ignore promise errors?  

========== Answer ==========  

The easiest and safest way to ignore promise errors is void that error. This
approach is ESLint friendly too.

```js
await promise.catch((e) => void e);
```

========== Id ==========  
423

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#423-What-is-the-easiest-way-to-ignore-promise

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
