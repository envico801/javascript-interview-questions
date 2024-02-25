==================== Question ====================  

### How do you perform form validation without javascript  

==================== Answer ====================  

You can perform HTML form validation automatically without using javascript. The
validation enabled by applying the `required` attribute to prevent form
submission when the input is empty.

```html
<form method="post">
  <input type="text" name="uname" required />
  <input type="submit" value="Submit" />
</form>
```

**Note:** Automatic form validation does not work in Internet Explorer 9 or
earlier.

==================== Id ====================  
273

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#273-How-do-you-perform-form-validation-without

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
