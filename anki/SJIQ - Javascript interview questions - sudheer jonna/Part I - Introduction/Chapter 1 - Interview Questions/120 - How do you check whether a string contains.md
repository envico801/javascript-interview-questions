========== Question ==========  

### How do you check whether a string contains a substring  

========== Answer ==========  

There are 3 possible ways to check whether a string contains a substring or not,

1. **Using includes:** ES6 provided `String.prototype.includes` method to test a
    string contains a substring

```javascript
var mainString = 'hello',
  subString = 'hell';
mainString.includes(subString);
```

1. **Using indexOf:** In an ES5 or older environment, you can use
    `String.prototype.indexOf` which returns the index of a substring. If the
    index value is not equal to -1 then it means the substring exists in the main
    string.

```javascript
var mainString = 'hello',
  subString = 'hell';
mainString.indexOf(subString) !== -1;
```

1. **Using RegEx:** The advanced solution is using Regular expression's test
    method(`RegExp.test`), which allows for testing for against regular
    expressions

```javascript
var mainString = 'hello',
  regex = /hell/;
regex.test(mainString);
```

========== Id ==========  
120

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#120-How-do-you-check-whether-a-string-contains

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
