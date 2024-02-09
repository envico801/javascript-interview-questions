==================== Question ====================  

### How do you remove falsy values from an array  

==================== Answer ====================  

You can apply the filter method on the array by passing Boolean as a parameter.
This way it removes all falsy values(0, undefined, null, false and "") from the
array.

```javascript
const myArray = [false, null, 1, 5, undefined];
myArray.filter(Boolean); // [1, 5] // is same as myArray.filter(x => x);
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#360-How-do-you-remove-falsy-values-from-an-arr

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
