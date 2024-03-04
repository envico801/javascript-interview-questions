========== Question ==========  

### How do you determine whether object is frozen or not  

========== Answer ==========  

Object.isFrozen() method is used to determine if an object is frozen or not.An
object is frozen if all of the below conditions hold true,

1. If it is not extensible.

2. If all of its properties are non-configurable.

3. If all its data properties are non-writable.

    The usage is going to be as follows,

```javascript
const object = {
  property: 'Welcome JS world',
};
Object.freeze(object);
console.log(Object.isFrozen(object));
```

========== Id ==========  
189

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#189-How-do-you-determine-whether-object-is-fro

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
