========== Question ==========  

### What are raw strings  

========== Answer ==========  

ES6 provides a raw strings feature using the `String.raw()` method which is used to get the raw string form of template strings. This feature allows you to access the raw strings as they were entered, without processing escape sequences. For example, the usage would be as below,

```javascript
var calculationString = String.raw`The sum of numbers is \n${1 + 2 + 3 + 4}!`;
console.log(calculationString); // The sum of numbers is \n10!
```

If you don't use raw strings, the newline character sequence will be processed by displaying the output in multiple lines

```javascript
var calculationString = `The sum of numbers is \n${1 + 2 + 3 + 4}!`;
console.log(calculationString);
// The sum of numbers is
// 10!
```

Also, the raw property is available on the first argument to the tag function

```javascript
function tag(strings) {
    console.log(strings.raw[0]);
}
```

========== Id ==========  
313

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#313-What-are-raw-strings

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
