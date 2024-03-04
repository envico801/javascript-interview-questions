========== Question ==========  

### How do you get the image width and height using JS  

========== Answer ==========  

You can programmatically get the image and check the dimensions(width and
height) using Javascript.

```javascript
var img = new Image();
img.onload = function () {
  console.log(this.width + 'x' + this.height);
};
img.src = 'http://www.google.com/intl/en_ALL/images/logo.gif';
```

========== Id ==========  
168

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#168-How-do-you-get-the-image-width-and-height

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
