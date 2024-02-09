==================== Question ====================  

### What is the difference between == and === operators  

==================== Answer ====================  

JavaScript provides both strict(===, !==) and type-converting(==, !=) equality
comparison. The strict operators take type of variable in consideration, while
non-strict operators make type correction/conversion based upon values of
variables. The strict operators follow the below conditions for different types,

1. Two strings are strictly equal when they have the same sequence of
   characters, same length, and same characters in corresponding positions.
2. Two numbers are strictly equal when they are numerically equal, i.e., having
   the same number value.  
   There are two special cases in this,
3. NaN is not equal to anything, including NaN.
4. Positive and negative zeros are equal to one another.
5. Two Boolean operands are strictly equal if both are true or both are false.
6. Two objects are strictly equal if they refer to the same Object.
7. Null and Undefined types are not equal with ===, but equal with ==, i.e,  
   null===undefined --> false, but null==undefined --> true  
   Some of the example which covers the above cases:

```javascript
   0 == false   // true
   0 === false  // false
   1 == "1"     // true
   1 === "1"    // false
   null == undefined // true
   null === undefined // false
   '0' == false // true
   '0' === false // false
   []==[] or []===[] //false, refer different objects in memory
   {}=={} or {}==={} //false, refer different objects in memory
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#9-What-is-the-difference-between-and

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
