========== Question ==========  

### How do you compare Object and Map  

========== Answer ==========  

**Objects** are similar to **Maps** in that both let you set keys to values,
retrieve those values, delete keys, and detect whether something is stored at a
key. Due to this reason, Objects have been used as Maps historically. But there
are important differences that make using a Map preferable in certain cases:

1. The keys of an Object can be Strings and Symbols, whereas they can be any
    value for a Map, including functions, objects, and any primitive.

2. The keys in a Map are ordered while keys added to Object are not. Thus, when
    iterating over it, a Map object returns keys in the order of insertion.

3. You can get the size of a Map easily with the size property, while the number
    of properties in an Object must be determined manually.

4. A Map is an iterable and can thus be directly iterated, whereas iterating
    over an Object requires obtaining its keys in some fashion and iterating over
    them.

5. An Object has a prototype, so there are default keys in an object that could
    collide with your keys if you're not careful. As of ES5 this can be bypassed
    by creating an object(which can be called a map) using `Object.create(null)`,
    but this practice is seldom done.

6. A Map may perform better in scenarios involving frequent addition and removal
    of key pairs.

========== Id ==========  
8

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#8-How-do-you-compare-object-and-map

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
