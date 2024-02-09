==================== Question ====================  

### How do you determine if an object is sealed or not  

==================== Answer ====================  

The Object.isSealed() method is used to determine if an object is sealed or not.
An object is sealed if all of the below conditions hold true

1. If it is not extensible.
2. If all of its properties are non-configurable.
3. If it is not removable (but not necessarily non-writable).  
   Let's see it in the action

```javascript
const object = {
  property: 'Hello, Good morning',
};
Object.seal(object); // Using seal() method to seal the object
console.log(Object.isSealed(object)); // checking whether the object is sealed or not
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#198-How-do-you-determine-if-an-object-is-seale

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
