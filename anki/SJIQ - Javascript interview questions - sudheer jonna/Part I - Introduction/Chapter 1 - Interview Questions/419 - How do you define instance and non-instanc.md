==================== Question ====================  

### How do you define instance and non-instance properties  

==================== Answer ====================  

The Instance properties must be defined inside of class methods. For example,
name and age properties defined inside constructor as below,

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}
```

But Static(class) and prototype data properties must be defined outside of the
ClassBody declaration. Let's assign the age value for Person class as below,

```javascript
Person.staticAge = 30;
Person.prototype.prototypeAge = 40;
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#419-How-do-you-define-instance-and-non-instanc

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
