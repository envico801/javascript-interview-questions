==================== Question ====================  

### What are tagged templates  

==================== Answer ====================  

Tagged templates are the advanced form of templates in which tags allow you to
parse template literals with a function. The tag function accepts the first
parameter as an array of strings and remaining parameters as expressions. This
function can also return manipulated strings based on parameters. Let's see the
usage of this tagged template behavior of an IT professional skill set in an
organization,

```javascript
var user1 = 'John';
var skill1 = 'JavaScript';
var experience1 = 15;
var user2 = 'Kane';
var skill2 = 'JavaScript';
var experience2 = 5;
function myInfoTag(strings, userExp, experienceExp, skillExp) {
  var str0 = strings[0]; // "Mr/Ms. "
  var str1 = strings[1]; // " is a/an "
  var str2 = strings[2]; // "in"
  var expertiseStr;
  if (experienceExp > 10) {
    expertiseStr = 'expert developer';
  } else if (skillExp > 5 && skillExp <= 10) {
    expertiseStr = 'senior developer';
  } else {
    expertiseStr = 'junior developer';
  }
  return `${str0}${userExp}${str1}${expertiseStr}${str2}${skillExp}`;
}
var output1 = myInfoTag`Mr/Ms. ${user1} is a/an ${experience1} in ${skill1}`;
var output2 = myInfoTag`Mr/Ms. ${user2} is a/an ${experience2} in ${skill2}`;
console.log(output1); // Mr/Ms. John is a/an expert developer in JavaScript
console.log(output2); // Mr/Ms. Kane is a/an junior developer in JavaScript
```

==================== Id ====================  
312

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#312-What-are-tagged-templates

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
