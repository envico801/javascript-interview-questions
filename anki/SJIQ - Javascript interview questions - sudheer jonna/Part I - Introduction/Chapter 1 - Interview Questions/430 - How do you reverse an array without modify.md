==================== Question ====================  

### How do you reverse an array without modifying original array  

==================== Answer ====================  

The `reverse()` method reverses the order of the elements in an array but it
mutates the original array. Let's take a simple example to demonistrate this
case,

```javascript
const originalArray = [1, 2, 3, 4, 5];
const newArray = originalArray.reverse();
console.log(newArray); // [ 5, 4, 3, 2, 1]
console.log(originalArray); // [ 5, 4, 3, 2, 1]
```

There are few solutions that won't mutate the original array. Let's take a look.

1. **Using slice and reverse methods:**  
   In this case, just invoke the `slice()` method on the array to create a
   shallow copy followed by `reverse()` method call on the copy.

```javascript
const originalArray = [1, 2, 3, 4, 5];
const newArray = originalArray.slice().reverse(); //Slice an array gives a new copy
console.log(originalArray); // [1, 2, 3, 4, 5]
console.log(newArray); // [ 5, 4, 3, 2, 1]
```

2. **Using spread and reverse methods:**  
   In this case, let's use the spread syntax (...) to create a copy of the array
   followed by `reverse()` method call on the copy.

```javascript
const originalArray = [1, 2, 3, 4, 5];
const newArray = [...originalArray].reverse();
console.log(originalArray); // [1, 2, 3, 4, 5]
console.log(newArray); // [ 5, 4, 3, 2, 1]
```

3. **Using reduce and spread methods:**  
   Here execute a reducer function on an array elements and append the
   accumulated array on right side using spread syntax

```javascript
const originalArray = [1, 2, 3, 4, 5];
const newArray = originalArray.reduce((accumulator, value) => {
  return [value, ...accumulator];
}, []);
console.log(originalArray); // [1, 2, 3, 4, 5]
console.log(newArray); // [ 5, 4, 3, 2, 1]
```

4. **Using reduceRight and spread methods:**  
   Here execute a right reducer function(i.e. opposite direction of reduce
   method) on an array elements and append the accumulated array on left side
   using spread syntax

```javascript
const originalArray = [1, 2, 3, 4, 5];
const newArray = originalArray.reduceRight((accumulator, value) => {
  return [...accumulator, value];
}, []);
console.log(originalArray); // [1, 2, 3, 4, 5]
console.log(newArray); // [ 5, 4, 3, 2, 1]
```

5. **Using reduceRight and push methods:**  
   Here execute a right reducer function(i.e. opposite direction of reduce
   method) on an array elements and push the iterated value to the accumulator

```javascript
const originalArray = [1, 2, 3, 4, 5];
const newArray = originalArray.reduceRight((accumulator, value) => {
  accumulator.push(value);
  return accumulator;
}, []);
console.log(originalArray); // [1, 2, 3, 4, 5]
console.log(newArray); // [ 5, 4, 3, 2, 1]
```

==================== Id ====================  
430
<!--ID: 1707879802560-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#430-How-do-you-reverse-an-array-without-modify

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
