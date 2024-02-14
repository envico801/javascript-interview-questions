==================== Question ====================  

### What are the different ways to create sparse arrays  

==================== Answer ====================  

There are 4 different ways to create sparse arrays in JavaScript

1. **Array literal:** Omit a value when using the array literal

```js
const justiceLeague = ['Superman', 'Aquaman', , 'Batman'];
console.log(justiceLeague); // ['Superman', 'Aquaman', empty ,'Batman']
```

2. **Array() constructor:** Invoking Array(length) or new Array(length)

```js
const array = Array(3);
console.log(array); // [empty, empty ,empty]
```

3. **Delete operator:** Using delete array[index] operator on the array

```js
const justiceLeague = ['Superman', 'Aquaman', 'Batman'];
delete justiceLeague[1];
console.log(justiceLeague); // ['Superman', empty, ,'Batman']
```

4. **Increase length property:** Increasing length property of an array

```js
const justiceLeague = ['Superman', 'Aquaman', 'Batman'];
justiceLeague.length = 5;
console.log(justiceLeague); // ['Superman', 'Aquaman', 'Batman', empty, empty]
```

==================== Id ====================  
428
<!--ID: 1707879803482-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#428-What-are-the-different-ways-to-create-spar

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
