==================== Question ====================  

### How do you decode or encode a URL in JavaScript  

==================== Answer ====================  

`encodeURI()` function is used to encode an URL. This function requires a URL
string as a parameter and return that encoded string.  
`decodeURI()` function is used to decode an URL. This function requires an
encoded URL string as parameter and return that decoded string.  
**Note:** If you want to encode characters such as `/ ? : @ & = + $ #` then you
need to use `encodeURIComponent()`.

```javascript
let uri = 'employeeDetails?name=john&occupation=manager';
let encoded_uri = encodeURI(uri);
let decoded_uri = decodeURI(encoded_uri);
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#23-How-do-you-decode-or-encode-a-url-in-javas

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
