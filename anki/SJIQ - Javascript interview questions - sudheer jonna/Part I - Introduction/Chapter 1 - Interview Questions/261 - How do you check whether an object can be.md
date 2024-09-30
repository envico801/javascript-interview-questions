========== Question ==========  

### How do you check whether an object can be extendable or not  

========== Answer ==========  

The `Object.isExtensible()` method is used to determine if an object is extendable or not. i.e, Whether it can have new properties added to it or not.

```javascript
const newObject = {};
console.log(Object.isExtensible(newObject)); //true
```

**Note:** By default, all the objects are extendable. i.e, The new properties can be added or modified.

========== Id ==========  
261

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#261-How-do-you-check-whether-an-object-can-be

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
