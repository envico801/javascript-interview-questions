========== Question ==========  

### What is the difference between dense and sparse arrays?  

========== Answer ==========  

An array contains items at each index starting from first(0) to
last(array.length - 1) is called as Dense array. Whereas if at least one item is
missing at any index, the array is called as sparse.

Let's see the below two kind of arrays,

```js
const avengers = ['Ironman', 'Hulk', 'CaptainAmerica'];
console.log(avengers[0]); // 'Ironman'
console.log(avengers[1]); // 'Hulk'
console.log(avengers[2]); // 'CaptainAmerica'
console.log(avengers.length); // 3
const justiceLeague = ['Superman', 'Aquaman', , 'Batman'];
console.log(justiceLeague[0]); // 'Superman'
console.log(justiceLeague[1]); // 'Aquaman'
console.log(justiceLeague[2]); // undefined
console.log(justiceLeague[3]); // 'Batman'
console.log(justiceLeague.length); // 4
```

========== Id ==========  
427

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#427-What-is-the-difference-between-dense-and-s

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
