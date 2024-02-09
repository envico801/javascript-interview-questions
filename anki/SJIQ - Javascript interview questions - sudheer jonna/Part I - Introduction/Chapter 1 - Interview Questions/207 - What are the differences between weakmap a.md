==================== Question ====================  

### What are the differences between WeakMap and Map  

==================== Answer ====================  

The main difference is that references to key objects in Map are strong while
references to key objects in WeakMap are weak. i.e, A key object in WeakMap can
be garbage collected if there is no other reference to it.  
Other differences are,

1. Maps can store any key type Whereas WeakMaps can store only collections of
   key objects
2. WeakMap does not have size property unlike Map
3. WeakMap does not have methods such as clear, keys, values, entries, forEach.
4. WeakMap is not iterable.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#207-What-are-the-differences-between-weakmap-a

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
