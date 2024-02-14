==================== Question ====================  

### How do you generate random integers  

==================== Answer ====================  

You can use Math.random() with Math.floor() to return random integers. For
example, if you want generate random integers between 1 to 10, the
multiplication factor should be 10,

```javascript
Math.floor(Math.random() * 10) + 1; // returns a random integer from 1 to 10
Math.floor(Math.random() * 100) + 1; // returns a random integer from 1 to 100
```

**Note:** Math.random() returns a random number between 0 (inclusive), and 1
(exclusive)

==================== Id ====================  
149
<!--ID: 1707879837456-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#149-How-do-you-generate-random-integers

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
