==================== Question ====================  

### What is the purpose of clearInterval method  

==================== Answer ====================  

The clearInterval() function is used in javascript to clear the interval which
has been set by setInterval() function. i.e, The return value returned by
setInterval() function is stored in a variable and it’s passed into the
clearInterval() function to clear the interval.  
For example, the below setInterval method is used to display the message for
every 3 seconds. This interval can be cleared by the clearInterval() method.

```javascript
<script>
var msg;
function greeting() {
   alert('Good morning');
}
function start() {
  msg = setInterval(greeting, 3000);
}
function stop() {
    clearInterval(msg);
}
</script>
```

==================== Id ====================  
118

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#118-What-is-the-purpose-of-clearinterval-metho

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
