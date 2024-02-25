==================== Question ====================  

### How do you load CSS and JS files dynamically  

==================== Answer ====================  

You can create both link and script elements in the DOM and append them as child
to head tag. Let's create a function to add script and style resources as below,

```javascript
function loadAssets(filename, filetype) {
  if (filetype == 'css') {
    // External CSS file
    var fileReference = document.createElement('link');
    fileReference.setAttribute('rel', 'stylesheet');
    fileReference.setAttribute('type', 'text/css');
    fileReference.setAttribute('href', filename);
  } else if (filetype == 'js') {
    // External JavaScript file
    var fileReference = document.createElement('script');
    fileReference.setAttribute('type', 'text/javascript');
    fileReference.setAttribute('src', filename);
  }
  if (typeof fileReference != 'undefined')
    document.getElementsByTagName('head')[0].appendChild(fileReference);
}
```

==================== Id ====================  
294

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#294-How-do-you-load-css-and-js-files-dynamical

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
