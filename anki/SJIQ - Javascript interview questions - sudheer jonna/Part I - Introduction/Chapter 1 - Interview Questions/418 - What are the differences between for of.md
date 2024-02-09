==================== Question ====================  

### What are the differences between for...of and for...in statements  

==================== Answer ====================  

Both for...in and for...of statements iterate over js data structures. The only
difference is over what they iterate:

1. for..in iterates over all enumerable property keys of an object
2. for..of iterates over the values of an iterable object.  
   Let's explain this difference with an example,

```javascript
let arr = ['a', 'b', 'c'];
arr.newProp = 'newVlue';
// key are the property keys
for (let key in arr) {
  console.log(key); // 0, 1, 2 & newValue
}
// value are the property values
for (let value of arr) {
  console.log(value); // a, b, c
}
```

Since for..in loop iterates over the keys of the object, the first loop logs 0,
1, 2 and newProp while iterating over the array object. The for..of loop
iterates over the values of a arr data structure and logs a, b, c in the
console.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#418-What-are-the-differences-between-for-of

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
