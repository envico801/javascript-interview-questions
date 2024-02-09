==================== Question ====================  

### What is the purpose of the array splice method  

==================== Answer ====================  

The **splice()** method adds/removes items to/from an array, and then returns
the removed item. The first argument specifies the array position/index for
insertion or deletion whereas the optional second argument indicates the number
of elements to be deleted. Each additional argument is added to the array.  
Some of the examples of this method are:

```javascript
let arrayIntegersOriginal1 = [1, 2, 3, 4, 5];
let arrayIntegersOriginal2 = [1, 2, 3, 4, 5];
let arrayIntegersOriginal3 = [1, 2, 3, 4, 5];
let arrayIntegers1 = arrayIntegersOriginal1.splice(0, 2); // returns [1, 2]; original array: [3, 4, 5]
let arrayIntegers2 = arrayIntegersOriginal2.splice(3); // returns [4, 5]; original array: [1, 2, 3]
let arrayIntegers3 = arrayIntegersOriginal3.splice(3, 1, 'a', 'b', 'c'); //returns [4]; original array: [1, 2, 3, "a", "b", "c", 5]
```

**Note:** Splice method modifies the original array and returns the deleted
array.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#6-What-is-the-purpose-of-the-array-splice-me

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
