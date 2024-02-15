==================== Question ====================  

### How do you find min and max value in an array  

==================== Answer ====================  

You can use `Math.min` and `Math.max` methods on array variables to find the
minimum and maximum elements within an array. Let's create two functions to find
the min and max value with in an array,

```javascript
var marks = [50, 20, 70, 60, 45, 30];
function findMin(arr) {
  return Math.min.apply(null, arr);
}
function findMax(arr) {
  return Math.max.apply(null, arr);
}
console.log(findMin(marks));
console.log(findMax(marks));
```

==================== Id ====================  
245
<!--ID: 1707879830325-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#245-How-do-you-find-min-and-max-value-in-an-ar

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
