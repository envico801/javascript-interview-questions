==================== Question ====================  

### What is a freeze method  

==================== Answer ====================  

The **freeze()** method is used to freeze an object. Freezing an object does not
allow adding new properties to an object,prevents from removing and prevents
changing the enumerability, configurability, or writability of existing
properties. i.e, It returns the passed object and does not create a frozen copy.

```javascript
const obj = {
  prop: 100,
};
Object.freeze(obj);
obj.prop = 200; // Throws an error in strict mode
console.log(obj.prop); //100
```

Remember freezing is only applied to the top-level properties in objects but not
for nested objects.  
For example, let's try to freeze user object which has employment details as
nested object and observe that details have been changed.

```javascript
const user = {
  name: 'John',
  employment: {
    department: 'IT',
  },
};
Object.freeze(user);
user.employment.department = 'HR';
```

**Note:** It causes a TypeError if the argument passed is not an object.

==================== Id ====================  
178
<!--ID: 1707879812591-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#178-What-is-a-freeze-method

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
