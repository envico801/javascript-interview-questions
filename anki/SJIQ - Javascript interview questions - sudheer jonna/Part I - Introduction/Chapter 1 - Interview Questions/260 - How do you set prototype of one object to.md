==================== Question ====================  

### How do you set prototype of one object to another  

==================== Answer ====================  

You can use the `Object.setPrototypeOf()` method that sets the prototype (i.e.,
the internal `Prototype` property) of a specified object to another object or
null. For example, if you want to set prototype of a square object to rectangle
object would be as follows,

```javascript
Object.setPrototypeOf(Square.prototype, Rectangle.prototype);
Object.setPrototypeOf({}, null);
```

==================== Id ====================  
260
<!--ID: 1707879829111-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#260-How-do-you-set-prototype-of-one-object-to

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
