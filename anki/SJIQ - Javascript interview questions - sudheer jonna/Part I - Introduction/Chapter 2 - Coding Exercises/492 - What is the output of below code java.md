==================== Question ====================  

### What is the output of below code

```javascript
const obj = { key: 'value' };
const array = [...obj];
console.log(array);
```

- 1: ['key', 'value']
- 2: TypeError
- 3: []
- 4: ['key']  

==================== Answer ====================  

##### Answer: 2

Spread syntax can be applied only to iterable objects. By default, Objects are
not iterable, but they become iterable when used in an Array, or with iterating
functions such as `map(), reduce(), and assign()`. If you still try to do it, it
still throws `TypeError: obj is not iterable`.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#492-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
