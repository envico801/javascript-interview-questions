==================== Question ====================  

### What are wrapper objects  

==================== Answer ====================  

Primitive Values like string,number and boolean don't have properties and
methods but they are temporarily converted or coerced to an object(Wrapper
object) when you try to perform actions on them. For example, if you apply
toUpperCase() method on a primitive string value, it does not throw an error but
returns uppercase of the string.

```javascript
let name = 'john';
console.log(name.toUpperCase()); // Behind the scenes treated as console.log(new String(name).toUpperCase());
```

i.e, Every primitive except null and undefined have Wrapper Objects and the list
of wrapper objects are String,Number,Boolean,Symbol and BigInt.

==================== Id ====================  
380
<!--ID: 1707879820317-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#380-What-are-wrapper-objects

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
