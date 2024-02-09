==================== Question ====================  

### How do you create an object with prototype  

==================== Answer ====================  

The Object.create() method is used to create a new object with the specified
prototype object and properties. i.e, It uses an existing object as the
prototype of the newly created object. It returns a new object with the
specified prototype object and properties.

```javascript
const user = {
  name: 'John',
  printInfo: function () {
    console.log(`My name is ${this.name}.`);
  },
};
const admin = Object.create(user);
admin.name = 'Nick'; // Remember that "name" is a property set on "admin" but not on "user" object
admin.printInfo(); // My name is Nick
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#202-How-do-you-create-an-object-with-prototype

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
