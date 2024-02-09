==================== Question ====================  

### What are nesting templates  

==================== Answer ====================  

The nesting template is a feature supported within template literals syntax to
allow inner backticks inside a placeholder ${ } within the template. For
example, the below nesting template is used to display the icons based on user
permissions whereas outer template checks for platform type,

```javascript
const iconStyles = `icon ${
  isMobilePlatform() ? '' : `icon-${user.isAuthorized ? 'submit' : 'disabled'}`
}`;
```

You can write the above use case without nesting template features as well.
However, the nesting template feature is more compact and readable.

```javascript
//Without nesting templates
const iconStyles = `icon ${
  isMobilePlatform() ? ''
  : user.isAuthorized ? 'icon-submit'
  : 'icon-disabled'
}`;
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#311-What-are-nesting-templates

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
