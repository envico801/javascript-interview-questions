========== Question ==========  

### How do you create copy to clipboard button  

========== Answer ==========  

You need to select the content(using .select() method) of the input element and execute the copy command with execCommand (i.e, execCommand('copy')). You can also execute other system commands like cut and paste.

```javascript
document.querySelector('#copy-button').onclick = function () {
    // Select the content
    document.querySelector('#copy-input').select();
    // Copy to the clipboard
    document.execCommand('copy');
};
```

========== Id ==========  
374

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#374-How-do-you-create-copy-to-clipboard-button

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
