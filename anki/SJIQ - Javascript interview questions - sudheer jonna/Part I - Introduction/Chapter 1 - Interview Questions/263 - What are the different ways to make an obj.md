========== Question ==========  

### What are the different ways to make an object non-extensible  

========== Answer ==========  

You can mark an object non-extensible in 3 ways,

1. Object.preventExtensions

2. Object.seal

3. Object.freeze

```javascript
var newObject = {};
Object.preventExtensions(newObject); // Prevent objects are non-extensible
Object.isExtensible(newObject); // false
var sealedObject = Object.seal({}); // Sealed objects are non-extensible
Object.isExtensible(sealedObject); // false
var frozenObject = Object.freeze({}); // Frozen objects are non-extensible
Object.isExtensible(frozenObject); // false
```

========== Id ==========  
263

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#263-What-are-the-different-ways-to-make-an-obj

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
