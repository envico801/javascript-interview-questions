==================== Question ====================  

### What is the output of below code

```javascript
var currentCity = 'NewYork';
var changeCurrentCity = function () {
  console.log('Current City:', currentCity);
  var currentCity = 'Singapore';
  console.log('Current City:', currentCity);
};
changeCurrentCity();
```

- 1: NewYork, Singapore
- 2: NewYork, NewYork
- 3: undefined, Singapore
- 4: Singapore, Singapore  

==================== Answer ====================  

Answer: 3  
Due to hositing feature, the variables declared with `var` will have `undefined`
value in the creation phase so the outer variable `currentCity` will get same
`undefined` value. But after few lines of code JavaScript engine found a new
function call(`changeCurrentCity()`) to update the current city with `var`
re-declaration. Since each function call will create a new execution context,
the same variable will have `undefined` value before the declaration and new
value(`Singapore`) after the declarion. Hence, the value `undefined` print first
followed by new value `Singapore` in the execution phase.

==================== Id ====================  
517
<!--ID: 1707879793886-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#517-What-is-the-output-of-below-code-jav

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
