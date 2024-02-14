==================== Question ====================  

### Why do you need to avoid with statement  

==================== Answer ====================  

JavaScript's with statement was intended to provide a shorthand for writing
recurring accesses to objects. So it can help reduce file size by reducing the
need to repeat a lengthy object reference without performance penalty. Let's
take an example where it is used to avoid redundancy when accessing an object
several times.

```javascript
a.b.c.greeting = 'welcome';
a.b.c.age = 32;
```

Using `with` it turns this into:

```javascript
with (a.b.c) {
  greeting = 'welcome';
  age = 32;
}
```

But this `with` statement creates performance problems since one cannot predict
whether an argument will refer to a real variable or to a property inside the
with argument.

==================== Id ====================  
302
<!--ID: 1707879810553-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#302-Why-do-you-need-to-avoid-with-statement

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
