==================== Question ====================  

### How to remove all line breaks from a string  

==================== Answer ====================  

The easiest approach is using regular expressions to detect and replace newlines
in the string. In this case, we use replace function along with string to
replace with, which in our case is an empty string.

```javascript
     function remove_linebreaks( var message ) {
         return message.replace( /[\r\n]+/gm, "" );
     }
```

In the above expression, g and m are for global and multiline flags.

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#354-How-to-remove-all-line-breaks-from-a-strin

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
