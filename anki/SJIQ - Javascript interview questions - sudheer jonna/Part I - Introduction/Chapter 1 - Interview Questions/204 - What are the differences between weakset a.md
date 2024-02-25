==================== Question ====================  

### What are the differences between WeakSet and Set  

==================== Answer ====================  

The main difference is that references to objects in Set are strong while
references to objects in WeakSet are weak. i.e, An object in WeakSet can be
garbage collected if there is no other reference to it.  
Other differences are,

1. Sets can store any value Whereas WeakSets can store only collections of
   objects
2. WeakSet does not have size property unlike Set
3. WeakSet does not have methods such as clear, keys, values, entries, forEach.
4. WeakSet is not iterable.

==================== Id ====================  
204

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#204-What-are-the-differences-between-weakset-a

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
