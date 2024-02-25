==================== Question ====================  

### Is that possible to use expressions in switch cases  

==================== Answer ====================  

You might have seen expressions used in switch condition but it is also possible
to use for switch cases by assigning true value for the switch condition. Let's
see the weather condition based on temparature as an example,

```js
const weather = (function getWeather(temp) {
  switch (true) {
    case temp < 0:
      return 'freezing';
    case temp < 10:
      return 'cold';
    case temp < 24:
      return 'cool';
    default:
      return 'unknown';
  }
})(10);
```

==================== Id ====================  
422

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#422-Is-that-possible-to-use-expressions-in-swi

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
