==================== Question ====================  

### How do you group and nest console output  

==================== Answer ====================  

The `console.group()` can be used to group related log messages to be able to
easily read the logs and use console.groupEnd()to close the group. Along with
this, you can also nest groups which allows to output message in hierarchical
manner.  
For example, if you’re logging a user’s details:

```js
console.group('User Details');
console.log('name: Sudheer Jonna');
console.log('job: Software Developer');
// Nested Group
console.group('Address');
console.log('Street: Commonwealth');
console.log('City: Los Angeles');
console.log('State: California');
// Close nested group
console.groupEnd();
// Close outer group
console.groupEnd();
```

You can also use `console.groupCollapsed()` instead of `console.group()` if you
want the groups to be collapsed by default.

==================== Id ====================  
426

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#426-How-do-you-group-and-nest-console-output

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
