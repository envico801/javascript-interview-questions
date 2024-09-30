========== Question ==========  

### How do style the console output using CSS?  

========== Answer ==========  

You can add CSS styling to the console output using the CSS format content specifier %c. The console string message can be appended after the specifier and CSS style in another argument. Let's print the red the color text using console.log and CSS specifier as below,

```js
console.log('%cThis is a red text', 'color:red');
```

It is also possible to add more styles for the content. For example, the font-size can be modified for the above text

```js
console.log(
    '%cThis is a red text with bigger font',
    'color:red; font-size:20px',
);
```

========== Id ==========  
424

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#424-How-do-style-the-console-output-using-css

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
