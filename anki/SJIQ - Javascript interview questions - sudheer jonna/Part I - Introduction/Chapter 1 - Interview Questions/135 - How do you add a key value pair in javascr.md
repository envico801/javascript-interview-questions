==================== Question ====================  

### How do you add a key value pair in javascript  

==================== Answer ====================  

There are two possible solutions to add new properties to an object. Let's take
a simple object to explain these solutions.

```javascript
var object = {
  key1: value1,
  key2: value2,
};
```

1. **Using dot notation:** This solution is useful when you know the name of the
   property

```javascript
object.key3 = 'value3';
```

1. **Using square bracket notation:** This solution is useful when the name of
   the property is dynamically determined.

```javascript
obj['key3'] = 'value3';
```

==================== Id ====================  
135
<!--ID: 1707879804414-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#135-How-do-you-add-a-key-value-pair-in-javascr

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
