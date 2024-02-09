==================== Question ====================  

### What is the output of below code

```javascript
var car = new Vehicle('Honda', 'white', '2010', 'UK');
console.log(car);
function Vehicle(model, color, year, country) {
  this.model = model;
  this.color = color;
  this.year = year;
  this.country = country;
}
```

- 1: Undefined
- 2: ReferenceError
- 3: null
- 4: {model: "Honda", color: "white", year: "2010", country: "UK"}  

==================== Answer ====================  

##### Answer: 4

The function declarations are hoisted similar to any variables. So the placement
for `Vehicle` function declaration doesn't make any difference.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 2 - Coding Exercises

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-2-Coding-Exercises::#450-What-is-the-output-of-below-code-java

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
